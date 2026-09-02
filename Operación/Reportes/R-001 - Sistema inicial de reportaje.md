---
tipo: reporte
estado: cerrado
revision_humana: aprobada
modulo: "[[Operación y reportaje de ACE]]"
tarea: "[[T-001 - Definir niveles de reportaje]]"
fecha: 2026-09-01
---

# Sistema inicial de reportaje

## Reporte del ejecutor

### Resumen

El sistema de reportaje de ACE quedó redefinido para registrar entregas significativas y sostener su revisión, no para producir un archivo después de cada tarea. Cada reporte responde a una tarea principal y reúne en un mismo hilo el resultado del ejecutor, la revisión, las correcciones y el cierre.

La propuesta original de niveles `ninguno`, `agente` y `equipo` fue reemplazada. Ya no existen propiedades de audiencia ni de nivel de reportaje. La necesidad de un reporte se decide por el valor de la entrega y por quién debe revisarla.

### Implicancias

- Terminar una tarea no crea un reporte automáticamente.
- Las revisiones `agente_externo`, `humano` o `equipo` requieren reporte; con `ejecutor` es opcional si el resultado merece una entrega separada.
- Un reporte sirve a humanos y agentes mediante resumen, detalle técnico opcional e hilo de revisión.
- La frecuencia sigue hitos, entregas, decisiones o revisiones reales.
- El apoyo visual es opcional y debe aportar evidencia o comprensión.

### Evidencia

- La convención vigente está en [[Sistema de reportaje ACE]].
- Frecuencia y eliminación de `audiencia` y `reportaje`: `f800abd docs: consolidate meaningful reports`.
- Criterio de contenido suficiente: `4d118df docs: define sufficient report content`.

### Abierto

- Validar la convención con [[T-014 - Probar el harness compartido en una tarea real]].
- Ajustarla solo si los casos reales revelan una necesidad concreta.

## Revisión

Tomás revisó y aprobó el reporte junto con los otros reportes estructurales abiertos. Antes del cierre se corrigieron las referencias a tareas para que coincidan con sus nombres reales.

## Enlaces

- [[Sistema de reportaje ACE]]
- [[Operación y reportaje de ACE]]
- [[T-001 - Definir niveles de reportaje]]
- [[T-014 - Probar el harness compartido en una tarea real]]
