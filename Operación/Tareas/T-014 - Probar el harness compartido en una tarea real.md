---
tipo: tarea
estado: en_curso
responsable: Fenrir
ejecutado_por: Fenrir
iniciativa: "[[Operación y reportaje de ACE]]"
revision: agente_externo
revisado_por:
resultado_revision: pendiente
creado: 2026-09-01
---

# Probar el harness compartido en una tarea real

Ejecutar una tarea acotada usando únicamente el contexto definido por el harness compartido.

## Criterio de aceptación

- El agente entiende su etapa y su foco, la tarea y la forma de reportar.
- Otro agente puede continuar usando solamente los artefactos registrados.
- Los vacíos reales del harness quedan anotados.

## Progreso

Se completaron dos turnos de una prueba aislada en Codex usando únicamente la autenticación local y el contexto del repositorio. El agente recuperó la etapa, el registro, la tarea y sus artefactos; orientó antes de actuar, conversó una corrección humana y no modificó el repositorio.

La prueba reveló dos ajustes acordados para el núcleo compartido: contextualizar la iniciación desde la etapa y las tareas relacionadas, y resolver la identidad mediante persistencia, inferencia contextual o pregunta directa al humano. La prueba real con el entorno habitual sigue pendiente.

## Reporte

[[R-013 - Piloto aislado del harness compartido]]
