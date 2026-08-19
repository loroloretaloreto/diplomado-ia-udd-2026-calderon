# Ficha de proyecto — Manorigen IA

## 1. Nombre interno
**Manorigen IA — Asistente para rotulación vehicular y personalización visual**

## 2. Problema
En proyectos de rotulación vehicular, la información crítica suele estar repartida entre mensajes, fotografías, medidas, archivos de diseño, observaciones del cliente y restricciones físicas del vehículo. Esto aumenta el riesgo de errores como cubrir una tapa de combustible, atravesar cortes de puertas, tapar emblemas, deformar una gráfica o producir con medidas incorrectas.

La propuesta busca usar IA como apoyo para ordenar requerimientos, detectar faltantes, resumir restricciones, registrar cambios y ayudar al equipo a verificar información antes de producir o instalar.

## 3. Usuario / cliente objetivo
Equipos de diseño, producción e instalación de una empresa gráfica como Manorigen, que gestionan proyectos de rotulación, impresión, personalización y producción visual.

## 4. Tipo de modelo
- [ ] Solo generativo
- [ ] Solo analítico
- [x] Pipeline combinado

**Analítico:** clasificación de solicitudes, extracción de medidas y restricciones, detección de urgencia y categorización de cambios.  
**Generativo:** síntesis de briefs, minutas, checklist de producción, propuestas de texto y documentación de proyecto.

## 5. Modelos candidatos
1. **Gemini Flash** — clasificación rápida y extracción de información desde mensajes.
2. **Gemini Pro** — razonamiento sobre briefs, transcripciones y documentación extensa.
3. **Modelo de embeddings** — búsqueda semántica de restricciones y casos similares.

## 6. Flujo propuesto
1. Ingreso de mensaje, brief, fotografía o reunión.
2. Extracción de cliente, vehículo, pieza, medidas, cambios y fecha.
3. Clasificación: solicitud, aprobación, corrección, consulta o mensaje sin acción.
4. Detección de restricciones técnicas.
5. Generación de resumen y checklist.
6. Validación humana.
7. Registro de versión aprobada.

## 7. Límites de la IA
La IA no debe aprobar por sí sola cambios de alcance, medidas de producción, decisiones creativas finales ni compromisos con el cliente. Debe indicar fuente, incertidumbre y permitir revisión humana.

## 8. Roadmap
- [x] Clase 22 — ficha de proyecto y experimentos iniciales.
- [x] Clase 23 — datasheet del dataset (`docs/datasheet_v1.md`).
- [x] Clase 24 — hallazgos NotebookLM (`docs/hallazgos_notebooklm.md`).
- [ ] Clase 25 — system prompt.
- [ ] Clase 26 — modelos HF candidatos.
- [ ] Clase 27 — sistema visual.
- [ ] Clase 28 — arquitectura del agente.
- [ ] Clase 29 — video generativo.
- [ ] Clase 30 — casos de uso Hermes.
- [ ] Clase 31 — cierre y Antigravity Loop.
