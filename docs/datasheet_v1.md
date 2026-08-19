# Datasheet v1 — Dataset de Gestión de Proyectos Creativos

**Proyecto:** Agencia de Diseño Gráfico y Comunicación Visual  
**Archivo:** `data/dataset_agencia_proyectos_v1.csv`

## 1. Propósito

Este dataset fue creado para explorar cómo una IA podría apoyar la gestión interna de una agencia de diseño, especialmente en la detección de información faltante, solicitudes de cambio, urgencias, aprobaciones y tareas que requieren seguimiento.

No busca reemplazar datos reales de producción ni entrenar un sistema final. Es un **dataset sintético de prototipado académico** construido para las actividades del Diplomado.

## 2. Unidad de análisis

Cada fila representa un evento o mensaje relacionado con un proyecto creativo: ingreso de brief, solicitud de cambio, aprobación, información faltante, urgencia, problema de producción o mensaje sin acción requerida.

## 3. Variables

- `id`: identificador del registro.
- `tipo_proyecto`: branding, gráfica vehicular, packaging, redes sociales, editorial, señalética, merchandising, etc.
- `canal`: correo, WhatsApp, reunión, formulario o sistema interno.
- `mensaje`: texto sintético que representa una comunicación típica.
- `categoria`: tipo de evento detectado.
- `urgencia`: baja, media o alta.
- `brief_completo`: sí/no/no_aplica.
- `requiere_accion`: sí/no.
- `rol_responsable`: rol que debería revisar o actuar.
- `estado`: pendiente, en_proceso, aprobado, resuelto o informativo.

## 4. Categorías

1. `brief_incompleto`
2. `solicitud_cambio`
3. `aprobacion`
4. `urgencia`
5. `produccion`
6. `consulta_cliente`
7. `sin_accion`
8. `entrega`

## 5. Origen de los datos

Los registros son **sintéticos**, redactados a partir de situaciones comunes identificadas en el proyecto académico de la agencia: briefs incompletos, cambios de cliente, información repartida entre distintos canales, problemas de coordinación y necesidad de trazabilidad.

No se incorporaron nombres reales, correos, teléfonos, montos, archivos de clientes ni información confidencial.

## 6. Uso previsto

El dataset puede servir para:

- probar reglas de clasificación;
- entrenar prototipos simples;
- explorar distribución de categorías;
- comparar urgencia y necesidad de acción;
- diseñar prompts de extracción estructurada;
- definir requerimientos para un futuro asistente IA.

## 7. Usos no previstos

No debe utilizarse como:

- evidencia estadística de comportamiento real de clientes;
- dataset productivo sin validación;
- base para decisiones automáticas sobre clientes o trabajadores;
- sustituto de observación con usuarios reales.

## 8. Posibles sesgos

El dataset refleja situaciones seleccionadas por el equipo del proyecto y puede sobrerrepresentar problemas que ya conocemos, como cambios y briefs incompletos. También simplifica el lenguaje de clientes y la complejidad de los proyectos reales.

Además, una categoría asignada a un mensaje puede depender del contexto. Por ejemplo, “cambiar el color” puede ser una solicitud válida, una exploración o una decisión ya aprobada. El sistema no debería interpretar automáticamente un cambio como definitivo sin confirmación.

## 9. Riesgos de automatización

- Falsos positivos de urgencia.
- Omitir un requisito crítico.
- Confundir una consulta con una instrucción.
- Propagar una clasificación incorrecta a tareas posteriores.
- Generar exceso de confianza en un estado “brief completo”.

## 10. Salvaguardas

- Mostrar el mensaje o fuente original junto a la clasificación.
- Permitir corrección humana.
- No aplicar cambios de alcance automáticamente.
- Mantener historial de cambios.
- Registrar quién confirmó una decisión.
- Etiquetar las inferencias como inferencias.

## 11. División sugerida

Para una prueba académica futura:

- 70% entrenamiento.
- 15% validación.
- 15% prueba.

Debido al tamaño reducido de esta versión, esta división es solo una referencia metodológica.

## 12. Mejoras futuras

- Incorporar más ejemplos y más variedad de lenguaje.
- Incluir mensajes ambiguos y casos límite.
- Crear anotación por dos personas para comparar acuerdo.
- Registrar fecha, proyecto y versión de la decisión en un dataset real anonimizado.
- Validar categorías con Coordinación de Proyectos y Dirección Creativa.

## 13. Conclusión

El dataset permite aterrizar el proyecto desde una idea general de “usar IA” hacia tareas concretas y evaluables. También hace visible que la calidad del sistema dependerá tanto del modelo como de la calidad, contexto y gobernanza de los datos que recibe.
