---
tipo: tarea
estado: pendiente
prioridad: media
responsable: Tomás y Ragnar
modulo: por_definir
revision: humano
revisado_por:
resultado_revision: pendiente
creado: 2026-09-02
---

# Validar el harness compartido en Claude Code

Comprobar en una sesión real de Claude Code que Ragnar puede usar el núcleo compartido de ACE sin instrucciones paralelas ni contexto conversacional heredado.

## Contexto

El harness ya fue validado con Fenrir en Codex y con Atreus y Mímir en Antigravity. `CLAUDE.md` importa `AGENTS.md`, pero todavía no existe una prueba real documentada equivalente en Claude Code.

## Incluye

- Iniciar desde una sesión nueva o sin historial relevante.
- Recuperar identidad, etapa, foco y contexto operativo desde las fuentes canónicas.
- Presentar la orientación inicial y conversar con el humano antes de implementar.
- Confirmar que `CLAUDE.md` carga el núcleo compartido sin duplicar reglas.
- Registrar solamente fricciones reales observadas durante la prueba.

## Criterio de aceptación

- Ragnar llega al contexto vigente y resuelve correctamente su identidad.
- La respuesta inicial explica la etapa y la situación lógica, no solo identificadores de tareas.
- El agente conversa y espera aprobación antes de modificar.
- La prueba permite decidir si el adaptador de Claude Code necesita cambios.

## Activación

Esta tarea pertenece al backlog transversal. Se asignará a un módulo vigente cuando el equipo decida ejecutarla.
