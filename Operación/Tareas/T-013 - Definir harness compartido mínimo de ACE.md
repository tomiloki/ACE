---
tipo: tarea
estado: revisión
responsable: Tomás y Fenrir
ejecutado_por: Fenrir
iniciativa: "[[Operación y reportaje de ACE]]"
revision: equipo
revisado_por:
resultado_revision: pendiente
creado: 2026-09-01
dependencia: "[[T-012 - Cerrar comunicación v0 entre agentes]]"
---

# Definir harness compartido mínimo de ACE

Convertir las reglas acordadas en instrucciones comunes para todos los agentes.

## Incluye

- Fuente de verdad, etapa y foco.
- Comunicación y reportaje.
- Revisión y conflictos.
- Estilo de documentación y respuesta.

## Contexto nuevo

Antes de escribir el harness, leer [[R-010 - Agentes, subagentes y etapas]]. El agente ya no tiene territorio: declara etapa y foco. El territorio quedó solo en los subagentes. Este documento cambió de vocabulario por esa razón.

## Criterio de aceptación

- Es corto y compartible entre Claude, Codex y Antigravity.
- Separa reglas comunes de instrucciones específicas por agente.
- No incorpora reglas todavía no conversadas.

## Resultado

- Núcleo común: [[AGENTS]].
- Adaptador de Claude Code: [[CLAUDE]].
- Adaptador de Antigravity: `.agents/rules/ace.md`.
- Las convenciones documentales no nucleares permanecen en [[Reglas de trabajo de Tomás]].
- La identidad se conserva en el contexto propio de cada agente y se valida contra [[Registro de agentes ACE]].

## Reporte

[[R-012 - Harness compartido mínimo de ACE]]
