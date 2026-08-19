# Datasheet v1 — Dataset de requerimientos de rotulación vehicular

**Clase 23 · Diplomado IA Aplicada al Diseño · UDD 2026**  
**Estudiante:** Loreto Calderón  
**Proyecto:** Manorigen IA — Asistente para rotulación vehicular y personalización visual

## 1. Nombre del dataset

**Manorigen Rotulación — Requerimientos y restricciones v1**

Archivos:
- `data/dataset_rotulacion_v1.csv`
- `data/dataset_rotulacion_v1.jsonl`

## 2. Motivación

El dataset fue creado para estudiar cómo una IA podría **clasificar y ordenar requerimientos** de un proyecto de rotulación vehicular. La intención no es entrenar una IA para diseñar de forma autónoma, sino explorar tareas de apoyo: identificar urgencia, etapa del proyecto, tipo de solicitud, presencia de restricciones técnicas y necesidad de revisión humana.

## 3. Composición

Contiene **30 registros sintéticos y anonimizados** inspirados en situaciones habituales de diseño, corrección, producción e instalación.

Distribución por etapa:
- Brief: 10
- Corrección: 11
- Producción: 9

Distribución por urgencia:
- Alta: 17
- Media: 9
- Baja: 4

## 4. Campos

| Campo | Descripción |
|---|---|
| `id` | Identificador artificial del registro. |
| `canal` | Canal por el que llega la observación: correo, WhatsApp o reunión. |
| `etapa` | Brief, corrección o producción. |
| `tipo_solicitud` | Categoría principal de la solicitud. |
| `texto` | Mensaje sintético que representa una observación del proyecto. |
| `urgencia` | Baja, media o alta. |
| `requiere_medicion` | 1 si la decisión necesita medidas o verificación física. |
| `restriccion_vehiculo` | Zona o condición del vehículo involucrada. |
| `riesgo_principal` | Riesgo que podría aparecer si la observación no se resuelve. |
| `decision_humana_requerida` | 1 si una persona debe validar antes de aplicar el cambio. |
| `tono` | Positivo, neutral o negativo; usado solo para práctica de clasificación. |

## 5. Cómo se generó

Los registros fueron redactados para representar situaciones comunes del flujo de rotulación. No contienen nombres de clientes, teléfonos, patentes, direcciones, fotografías privadas ni datos comerciales reales. Se usaron ejemplos genéricos y se mantuvo únicamente la lógica del problema.

## 6. Etiquetado

Las etiquetas fueron asignadas manualmente con criterios simples:

- **Urgencia alta:** puede afectar producción, instalación, datos finales, medidas o funcionalidad.
- **Urgencia media:** corrección importante de composición o ubicación, pero no bloquea por sí sola toda la producción.
- **Urgencia baja:** mejora visual o de jerarquía que puede resolverse sin riesgo técnico inmediato.
- **Decisión humana requerida:** se marca cuando la IA no debería aplicar el cambio sin revisión de diseño, producción o cliente.

## 7. Usos recomendados

- Clasificar feedback por etapa y urgencia.
- Detectar mensajes que mencionan restricciones físicas.
- Probar embeddings y agrupación de conceptos.
- Diseñar un checklist de brief y producción.
- Analizar sesgos de un clasificador simple.

## 8. Usos no recomendados

- Aprobar diseños automáticamente.
- Definir medidas reales a partir del texto.
- Sustituir inspección del vehículo.
- Inferir intención emocional del cliente.
- Entrenar un sistema productivo con este dataset pequeño y sintético.

## 9. Sesgos y limitaciones

1. El dataset refleja principalmente el punto de vista de una empresa de diseño y producción gráfica, no toda la diversidad del mercado.
2. Hay una cantidad alta de situaciones de riesgo técnico porque ese es el foco del proyecto; un modelo podría aprender a sobrerrepresentar la urgencia.
3. Los textos fueron redactados de manera relativamente clara. En la realidad existen mensajes incompletos, audios, errores ortográficos, contradicciones y ambigüedad.
4. El tamaño es demasiado pequeño para entrenamiento real; sirve para experimentación y documentación.
5. Las categorías fueron definidas por una persona y por lo tanto incorporan decisiones humanas.

## 10. Privacidad y ética

El dataset es sintético. Si en una fase futura se incorporan conversaciones reales, deben eliminarse datos personales y comerciales, pedir autorización cuando corresponda y definir retención, acceso y uso antes de subir material a servicios externos.

## 11. Validación humana

Toda predicción relacionada con medidas, cortes, materiales, identidad, datos de contacto, zonas de apertura o producción debe ser validada por una persona responsable.

## 12. Versión

**v1 · agosto 2026**. Esta versión se conserva como evidencia académica y puede ampliarse en clases posteriores.
