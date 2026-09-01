---
tipo: reporte
estado: abierto
iniciativa: "[[Operación y reportaje de ACE]]"
tarea: "[[T-014 - Probar el harness compartido en una tarea real]]"
fecha: 2026-09-01
---

# Piloto aislado del harness compartido

## Reporte del ejecutor

### Resumen

Se ejecutaron dos turnos de T-014 en una sesión Codex aislada de configuración global, plugins, Engram e historial previo. El único contexto operativo disponible fue el repositorio. El agente recuperó la etapa E-001, el registro, T-013, T-014, R-012 y el sistema de reportaje; presentó orientación, respondió a dudas humanas y esperó aprobación antes de modificar.

La iniciación fue enfocada y accionable. La conversación posterior corrigió una interpretación sobre identidad, descartó crear una segunda tarea artificial y estableció que T-014 puede probar el propio ciclo operativo del harness.

### Evidencia

| Medición | Turno 1 | Turno 2 incremental | Total acumulado |
|---|---:|---:|---:|
| Input | 83.570 | 29.888 | 113.458 |
| Input cacheado | 69.632 | 23.296 | 92.928 |
| Input no cacheado | 13.938 | 6.592 | 20.530 |
| Output | 820 | 710 | 1.530 |
| Reasoning output | 125 | 196 | 321 |

- Prompt inicial exacto: `Quiero hacer T-014.`
- La sesión leyó únicamente y el estado de Git no cambió en ninguno de los dos turnos.
- El segundo turno reutilizó gran parte del contexto mediante caché.
- Codex advirtió que acortó descripciones de skills por presupuesto de contexto incluso sin configuración global; parte relevante de la carga pertenece al entorno base y no al harness.

### Hallazgos

- La orientación debe explicar en lenguaje humano qué intenta dejar resuelto la etapa vigente, qué avances recientes construyeron la situación actual y por qué la tarea activa sigue lógicamente de ellos. Los identificadores son referencias; no reemplazan ese contexto ni obligan a explicar el proyecto general.
- La identidad puede inferirse cuando convergen el humano asociado a la cuenta, la tarea, el responsable, la plataforma, la etapa, el foco y el historial.
- Si la inferencia no es inequívoca, el agente debe preguntarle directamente al humano. No debe continuar sin identidad.
- T-014 puede ser su propio piloto: activa, recupera contexto, orienta, conversa, registra evidencia y deja continuidad para otro agente.
- El agente aceptó la corrección humana, explicó su razonamiento y reformuló el curso sin actuar antes de la aprobación.

### Ajustes aplicados

`AGENTS.md` fue precisado para:

- resolver identidad mediante persistencia, inferencia contextual o conversación con el humano;
- contextualizar la iniciación desde la etapa y las tareas que explican la situación actual.

### Abierto

- Ejecutar una prueba real con el entorno habitual y comparar respuesta, adherencia y consumo.
- Incorporar cualquier nuevo vacío antes de revisar el cierre de T-013.
- Someter T-014 a revisión por un agente externo cuando su ejecución esté completa.

## Revisión

Pendiente. El reporte permanece abierto mientras continúa la prueba real.

## Enlaces

- [[T-014 - Probar el harness compartido en una tarea real]]
- [[T-013 - Definir harness compartido mínimo de ACE]]
- [[R-012 - Harness compartido mínimo de ACE]]
- [[AGENTS]]
- [[E-001 - Ecosistema]]
- [[Registro de agentes ACE]]
