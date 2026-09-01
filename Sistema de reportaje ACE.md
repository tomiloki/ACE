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

## Un hilo por tarea principal

Cada reporte responde a una tarea principal y concentra en el mismo archivo:

1. Reporte del ejecutor.
2. Revisión.
3. Correcciones, si fueron solicitadas.
4. Revisiones posteriores hasta el cierre.

El reporte funciona como un hilo: la revisión no crea otro archivo. Puede enlazar otras tareas como contexto, pero solo gobierna el cierre de su tarea principal.

El reporte y la tarea conservan su propio estado. Cuando el reporte se cierra, la tarea principal se marca como terminada. Si la revisión solicita cambios, el reporte permanece abierto y la tarea vuelve a ejecución.

Cuando la revisión es humana, un usuario puede cerrar el reporte manualmente. No se exige aprobación de todos los integrantes ni un proceso de consenso.

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
- Cada reporte gobierna una tarea principal; puede enlazar otras como contexto.
- El reporte enlaza documentación, decisiones, issues y evidencias; no las copia.

Los niveles, frecuencia y destinatarios del reportaje requieren una conversación posterior antes de considerarse cerrados.

## Revisión de tareas

La revisión completa vive dentro del reporte de la tarea. No tiene módulo ni archivo propio. La tarea conserva las propiedades resumidas necesarias para mostrar su estado.

| Campo | Uso |
|---|---|
| `ejecutado_por` | Persona o agente que realizó el trabajo |
| `revision` | `ninguna`, `agente`, `humano` o `equipo` |
| `revisor_requerido` | Quién debe revisar |
| `revisado_por` | Quién revisó finalmente |
| `resultado_revision` | `pendiente`, `aprobada` o `cambios_solicitados` |

### Reglas

- Si revisa un agente, debe ser distinto del ejecutor.
- El revisor informa; no corrige silenciosamente.
- Una tarea con revisión requerida no termina antes de ser aprobada.
- El revisor agrega sus conclusiones al mismo reporte.
- Si solicita cambios, el ejecutor responde y registra la corrección en ese mismo hilo.
- El alcance, evidencia y determinismo de las revisiones por agentes o subagentes se definirán más adelante.
