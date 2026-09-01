---
tipo: estado_proyecto
estado: vigente
actualizado: 2026-09-01
---

# Estado actual del ecosistema ACE

## Dónde estamos

- Obsidian funciona como libreta operativa compartida.
- Git local protege el historial; todavía no existe remoto.
- La etapa vigente es [[E-001 - Ecosistema]]; el foco de cada agente vive en [[Registro de agentes ACE]].
- Las tareas, iniciativas y reportes viven en `Operación/` y se consultan desde [[Panel ACE]].

## Fundamentos definidos

- Harness operativo universal en [[AGENTS]] y convenciones documentales en [[Reglas de trabajo de Tomás]].
- Mapa general del ecosistema.
- El reporte no nace por cada tarea: aparece ante una entrega significativa o una revisión distinta del ejecutor.
- Un reporte por tarea principal, con resumen humano, detalle técnico opcional e hilo de revisión.
- Revisión recomendada por quién revisa: ejecutor, agente externo, humano o equipo.
- Agentes con etapa y foco; subagentes con territorio fijo.
- Identidades temporales: Ragnar, Fenrir, Atreus y Mímir como agentes; Heimdall como subagente.

## Último avance

Fenrir implementó el harness compartido mínimo. `AGENTS.md` es el núcleo canónico; Claude Code lo importa desde `CLAUDE.md` y Antigravity lo referencia desde una regla de workspace. La identidad permanece en el contexto propio de cada agente y se valida contra el registro.

- [[T-013 - Definir harness compartido mínimo de ACE]]
- [[R-012 - Harness compartido mínimo de ACE]]

T-013 quedó pendiente de revisión de equipo. T-014 validará la carga efectiva y el consumo de contexto en una tarea real.

### Avance de reportaje

Se simplificaron revisión y reportaje. La revisión recomienda quién revisa y puede cambiar después de implementar. El reporte ya no nace por cada tarea ni distingue audiencia: aparece ante resultados significativos o revisiones distintas del ejecutor y combina resumen humano, detalle técnico opcional e hilo de revisión.

- [[Sistema de reportaje ACE]]

Se eliminaron `revisor_requerido`, `reportaje` y `audiencia`. No se lanzó ninguna revisión.

### Activación y continuidad

Fenrir implementó la activación y continuidad v0. Tomás sigue siendo el router: el agente recupera contexto, presenta un reporte inteligente de iniciación, conversa y espera aprobación explícita. La entrega y revisión quedan en un único reporte por tarea principal.

- [[T-012 - Cerrar comunicación v0 entre agentes]]
- [[R-011 - Activación y continuidad v0]]

Tomás cerró T-012 manualmente, sin lanzar revisión por agente o subagente.

## Avance anterior

Ragnar separó agentes de subagentes. El agente declara etapa y foco; el subagente conserva territorio fijo. Se eliminó el territorio de los agentes, que estaba duplicado en tres documentos.

- [[T-016 - Separar agentes de subagentes]]
- [[R-010 - Agentes, subagentes y etapas]]

**Aviso a Fenrir.** El cambio tocó [[Mapa del ecosistema ACE]] y [[Reglas de trabajo de Tomás]], donde Fenrir venía trabajando, con autorización directa de Tomás y sin acuerdo previo. También cambió el vocabulario de [[T-013 - Definir harness compartido mínimo de ACE]] y [[T-014 - Probar el harness compartido en una tarea real]]. Los detalles están en [[R-010 - Agentes, subagentes y etapas]].

## Avance previo

Fenrir implementó identidades y revisión cruzada. Heimdall pidió cambios en una primera revisión y aprobó la segunda.

- [[T-011 - Probar revisión cruzada entre agentes]]
- [[R-008 - Identidades y revisión cruzada]]
- [[R-009 - Piloto de revisión cruzada]]

## Siguiente orden

1. Revisar en equipo [[T-013 - Definir harness compartido mínimo de ACE]] y [[R-012 - Harness compartido mínimo de ACE]].
2. [[T-014 - Probar el harness compartido en una tarea real]].
3. Ajustar el harness solamente si el piloto revela un vacío real.

## Más adelante

- [[T-015 - Profundizar el harness de Heimdall]]
- Preparar la estructura base del repositorio compartido.
- Publicar en GitHub cuando la base esté madura.

Relacionado: [[E-001 - Ecosistema]] · [[Mapa del ecosistema ACE]] · [[Registro de agentes ACE]] · [[Registro de subagentes ACE]] · [[Sistema de reportaje ACE]]
