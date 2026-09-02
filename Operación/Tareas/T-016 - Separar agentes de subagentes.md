---
tipo: tarea
estado: terminada
responsable: Tomás y Ragnar
ejecutado_por: Ragnar
modulo: "[[Operación y reportaje de ACE]]"
revision: humano
revisado_por: Tomás
resultado_revision: aprobada
creado: 2026-09-01
---

# Separar agentes de subagentes

Distinguir al agente que conversa con el usuario del subagente que se invoca, y reemplazar el territorio fijo de los agentes por etapa y foco.

## Incluye

- Registro de agentes con etapa y foco.
- Registro de subagentes con territorio fijo.
- Documento de etapa que se conserva al cerrarse.
- Eliminación del territorio duplicado en mapa, reglas y estado.

## Criterio de aceptación

- El territorio de los agentes deja de existir y queda una sola fuente del foco.
- La etapa orienta y no restringe, y está escrito de forma explícita.
- Heimdall queda registrado como subagente.
- Las etapas cerradas se conservan.

## Resultado

- Nuevos: [[E-001 - Ecosistema]], [[Registro de subagentes ACE]].
- Modificados: [[Registro de agentes ACE]], [[Mapa del ecosistema ACE]], [[Reglas de trabajo de Tomás]], [[Estado actual del ecosistema ACE]], [[Heimdall - Revisión independiente]].

## Reporte

[[R-010 - Agentes, subagentes y etapas]]
