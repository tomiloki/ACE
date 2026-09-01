---
tipo: registro_subagentes
estado: propuesta
---

> Un subagente se invoca, ejecuta un contrato y termina. No conversa con el usuario.

| Subagente    | Territorio             | Invocable por    | Harness                            |
| ------------ | ---------------------- | ---------------- | ---------------------------------- |
| **Heimdall** | Revisión independiente | Cualquier agente | [[Heimdall - Revisión independiente]] |

## Identidad de subagente

Cada subagente define:

- Nombre.
- Territorio fijo.
- Entrada mínima.
- Salida con formato definido.
- Reglas.

## Diferencias con un agente

- No tiene humano responsable.
- No tiene etapa ni foco: su territorio es su definición y no cambia con la etapa del proyecto.
- No mantiene conversación ni decide; entrega una salida y termina.
- No pertenece a ningún agente. El contrato es el mismo desde cualquier plataforma.

Si un subagente necesitara una etapa, sería señal de que en realidad es un agente.

Relacionado: [[Registro de agentes ACE]]
