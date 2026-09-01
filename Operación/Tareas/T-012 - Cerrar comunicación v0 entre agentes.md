---
tipo: tarea
estado: en_curso
responsable: Tomás y Fenrir
ejecutado_por: Fenrir
iniciativa: "[[Operación y reportaje de ACE]]"
reportaje: equipo
revision: humano
revisor_requerido: Tomás
revisado_por:
resultado_revision: pendiente
creado: 2026-09-01
---

# Cerrar comunicación v0 entre agentes

Definir el flujo mínimo de activación humana, orientación, aprobación, entrega y continuidad.

## Flujo acordado

1. Tomás activa y enruta al agente.
2. El agente recupera y verifica contexto sin modificar artefactos.
3. Presenta un reporte inteligente de iniciación en la conversación.
4. Usuario y agente conversan alternativas e implicancias.
5. El agente ejecuta solo después de aprobación explícita.
6. La entrega y sus revisiones continúan dentro de un único reporte ligado a la tarea principal.

## Caso real registrado

2026-09-01. Ragnar cambió [[Mapa del ecosistema ACE]] y [[Reglas de trabajo de Tomás]], donde venía trabajando Fenrir, con autorización directa de Tomás. Para avisarle no existió canal: el aviso se escribió en [[Estado actual del ecosistema ACE]] y dentro de [[T-013 - Definir harness compartido mínimo de ACE]], y depende de que alguien abra esas notas.

El caso no requiere mensajería ni activación automática entre agentes. El cambio debe quedar en la tarea y el reporte afectados; Tomás activa al siguiente agente y este recupera el contexto antes de actuar.

## Límites de v0

- No crea bandeja, mensajes ni identificadores de comunicación.
- No persiste el reporte de iniciación: ocurre en tiempo real con el usuario.
- No automatiza agentes ni permite que se activen mutuamente.
- No profundiza todavía niveles, frecuencia ni destinatarios del reportaje.
- No define todavía cómo se ejecutan y evidencian las revisiones por agentes o subagentes.

## Criterio de aceptación

- El flujo es breve y ejecutable.
- Mantiene al humano al mando y evita ejecución sin conversación previa.
- Reutiliza tareas, reportes y documentación sin crear otra fuente de verdad.
- Tomás lo revisa antes de adoptarlo.

## Resultado

- [[Reglas de trabajo de Tomás]]
- [[Sistema de reportaje ACE]]
- [[R-011 - Activación y continuidad v0]]

Implementado y pendiente de revisión de Tomás.
