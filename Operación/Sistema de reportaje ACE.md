# Sistema de reportaje ACE

> Estado: vigente; se validará y ajustará con casos reales.

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

## Cuándo existe

Terminar una tarea no crea automáticamente un reporte.

- Si `revision` recomienda `agente_externo`, `humano` o `equipo`, la tarea necesita reporte porque la revisión ocurre en ese hilo.
- Si recomienda `ejecutor`, el reporte es opcional y se crea solo cuando el resultado merece entregarse o conservarse por separado.
- Una tarea pequeña puede cerrarse con su propio registro cuando la tarea y Git explican suficientemente el resultado.
- Varias tareas menores pueden alimentar un solo resultado significativo gobernado por una tarea principal.

## Frecuencia

La frecuencia sigue entregas significativas, hitos, revisiones necesarias, decisiones pendientes o checkpoints solicitados por el usuario. No se crea un reporte por día, sesión, cantidad de tareas ni cambio pequeño.

## Contenido en capas

Cada reporte sirve a humanos y agentes sin clasificar audiencia ni crear versiones separadas.

### Resumen

Breve y orientado al humano:

- Resultado.
- Implicancias relevantes.
- Estado actual.
- Decisiones o revisiones pendientes.
- Cómo revisar, cuando corresponda.

### Detalle técnico

Opcional y sin repetir el resumen:

- Archivos o componentes afectados.
- Decisiones técnicas.
- Evidencia y verificaciones.
- Limitaciones, riesgos y asuntos abiertos.
- Información necesaria para que otro agente continúe.

### Revisión

El mismo archivo conserva las conclusiones del revisor, correcciones del ejecutor y revisiones posteriores hasta el cierre.

## Criterio de suficiencia

Un reporte es suficiente cuando permite comprender el resultado, tomar una decisión, revisar el trabajo o continuarlo sin reconstruir la tarea completa.

El agente comprueba que el reporte responda, cuando corresponda:

1. ¿Qué resultado existe ahora?
2. ¿Qué cambió o qué implica?
3. ¿Cómo se verificó o qué evidencia existe?
4. ¿Qué quedó abierto?
5. ¿Qué debe decidir, revisar o hacer alguien ahora?

Estas preguntas no son secciones obligatorias. Si algo no aplica, se omite; no se agrega relleno para completar una plantilla.

## Apoyo visual

El apoyo visual es opcional. Se agrega solamente cuando demuestra un resultado, facilita su revisión, compara antes y después o simplifica algo difícil de explicar. No se crean diagramas o capturas decorativas.

## Reglas

- Cada reporte gobierna una tarea principal; puede enlazar otras como contexto.
- El reporte enlaza documentación, decisiones, issues y evidencias; no las copia.
- No existe propiedad `audiencia` ni nivel `reportaje`.

## Revisión de tareas

La revisión completa vive dentro del reporte de la tarea. No tiene módulo ni archivo propio. La tarea conserva las propiedades resumidas necesarias para mostrar su estado.

| Campo | Uso |
|---|---|
| `ejecutado_por` | Persona o agente que realizó el trabajo |
| `revision` | Recomendación vigente: `ejecutor`, `agente_externo`, `humano` o `equipo` |
| `revisado_por` | Quién revisó finalmente |
| `resultado_revision` | `pendiente`, `aprobada` o `cambios_solicitados` |

### Recomendación de revisión

La revisión se recomienda por quién debería realizarla, no por el tamaño o complejidad de la tarea.

| Recomendación | Uso |
|---|---|
| `ejecutor` | El propio ejecutor verifica un cambio acotado, reversible y de bajo impacto. |
| `agente_externo` | Revisa un agente o subagente distinto del ejecutor. Quien tome la revisión elige la entidad concreta. |
| `humano` | Requiere criterio, contexto, validación visual, de negocio u otra decisión humana. |
| `equipo` | Define fundamentos compartidos: arquitectura, stack, modelo de datos, producto u otra base imprescindible. |

La recomendación inicial se registra al crear la tarea. Después de implementar, el ejecutor puede mantenerla o recomendar otra categoría según el resultado real. El usuario decide cómo se revisará; cambiar la recomendación no dispara una revisión automáticamente.

Las tareas históricas sin `revision` no se categorizan retroactivamente. Si se retoman, reciben una recomendación durante su nueva orientación.

### Reglas

- Si la recomendación es `agente_externo`, quien revisa debe ser distinto del ejecutor.
- `equipo` no implica votación, unanimidad ni estados por integrante; el equipo conversa y un humano registra el resultado.
- El revisor informa; no corrige silenciosamente.
- Si el usuario decide realizar la revisión recomendada, la tarea no termina hasta resolverla.
- El revisor agrega sus conclusiones al mismo reporte.
- Si solicita cambios, el ejecutor responde y registra la corrección en ese mismo hilo.
- El alcance, evidencia y determinismo de las revisiones por agentes o subagentes se definirán más adelante.
