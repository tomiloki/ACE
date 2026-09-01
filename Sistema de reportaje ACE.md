# Sistema de reportaje ACE

> Estado: propuesta en conversación.

## Propósito

El reporte resume:

- Qué pasó.
- Por qué.
- Implicancias relevantes.
- Estado actual.
- Enlaces al contenido real.

El reporte **no contiene ni duplica el trabajo**.

## Nivel definido por tarea

| Nivel | Uso | Revisión humana | Apoyo visual |
|---|---|---:|---:|
| Ninguno | Cambio trivial o suficientemente registrado por la tarea | No | No |
| Agente | Continuidad, trazabilidad o contexto para otros agentes | No | Opcional |
| Equipo | Cambio que el equipo debe comprender, revisar o decidir | Sí | Obligatorio |

## Reporte para agentes

- Breve y estructurado.
- Puede vivir en una issue, comentario o nota enlazada.
- Prioriza continuidad entre agentes.
- No requiere revisión del equipo.

## Reporte para el equipo

- Breve y entendible sin revisar todo el trabajo.
- Requiere revisión humana.
- Incluye un anexo o material visual: diagrama, captura, tabla, demo u otro apoyo adecuado.
- Mantiene una versión Markdown legible por agentes.

## Criterio inicial

**Ninguno**
- Trabajo local, trivial o reversible.
- El check de la tarea entrega suficiente trazabilidad.

**Agente**
- Otro agente necesitará conocer el cambio.
- Afecta trabajo posterior, pero no requiere evaluación humana.

**Equipo**
- Cambia dirección, arquitectura o coordinación.
- Completa un hito relevante.
- Introduce un riesgo o decisión importante.
- Afecta a varias áreas, al cliente o a Duoc.

## Reglas

- El nivel se define al crear la tarea.
- Puede escalarse si aumenta su relevancia o así lo considera el usuario al momento de implementar la tarea.
- Un reporte de equipo también sirve como reporte para agentes.
- Varias tareas pueden consolidarse en un solo reporte de iniciativa.
- El reporte enlaza documentación, decisiones, issues y evidencias; no las copia.
