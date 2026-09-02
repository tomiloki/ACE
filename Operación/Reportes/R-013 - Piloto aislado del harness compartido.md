---
tipo: reporte
estado: cerrado
revision_humana: aprobada
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

### Prueba real

Atreus y Mímir iniciaron trabajo desde Antigravity con sus entornos habituales y sin el historial conversacional de Fenrir. Ambos recuperaron E-001, los avances estructurales recientes y alternativas de continuidad. Además:

- Atreus identificó la validación del harness en Antigravity y la revisión de T-013 como próximos pasos relevantes.
- Mímir completó onboarding, verificó escritura local y publicó su prueba mediante GitHub.
- Atreus preparó propuestas versionadas para la Fase 1 Duoc; ese uso real reveló la necesidad de un espacio compartido no canónico, resuelta posteriormente mediante `Borradores/`.
- Las respuestas mantuvieron al humano dentro de la conversación y no saltaron automáticamente a implementar.

El posible sesgo hacia tareas y ejecución queda como observación, no como defecto confirmado: los agentes pudieron también orientar, proponer y conversar. Se ajustará únicamente si el uso sostenido demuestra una fricción recurrente.

## Revisión

Atreus y Mímir actuaron como validadores externos al ejecutor original y demostraron continuidad usando los artefactos registrados. Tomás revisó las respuestas, aprobó su calidad y decidió congelar la estructura en lugar de seguir refinándola por hipótesis.

Los criterios de aceptación de T-014 se consideran cumplidos y el reporte queda cerrado.

## Enlaces

- [[T-014 - Probar el harness compartido en una tarea real]]
- [[T-013 - Definir harness compartido mínimo de ACE]]
- [[R-012 - Harness compartido mínimo de ACE]]
- [[AGENTS]]
- [[E-001 - Ecosistema]]
- [[Registro de agentes ACE]]
