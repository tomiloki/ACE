# Módulos de trabajo de ACE

Los módulos son frentes de trabajo paralelizables dentro de una etapa. Permiten agrupar y asignar tareas que persiguen un resultado relacionado sin convertir cada frente en una etapa separada.

La estructura operativa es:

```text
Proyecto
└── Etapa vigente
    └── Módulos de trabajo
        └── Tareas
            └── Reporte, cuando corresponda
```

## Etapa

La etapa representa el tramo global y secuencial del proyecto. Explica qué intenta dejar resuelto el equipo antes de avanzar y conserva un criterio de cierre. Solo una etapa está vigente a la vez.

## Módulo

El módulo representa un frente concreto dentro de una etapa. Tiene propósito, estado y responsables; agrupa tareas relacionadas y puede cerrarse independientemente de los demás módulos.

En ACE, `módulo` significa **módulo de trabajo**, no necesariamente componente técnico o módulo de código.

## Tarea

Cada tarea pertenece a un solo módulo principal mediante la propiedad `modulo`. Si afecta otros frentes, los enlaza como contexto, pero conserva un único módulo para evitar responsabilidad y estado ambiguos.

La tarea hereda su etapa desde el módulo:

```text
Tarea → Módulo → Etapa
```

Por esa razón, la etapa no se repite en cada tarea.

## Convención mínima

Un módulo usa:

```yaml
tipo: modulo
estado: activo
etapa: "[[E-000 - Nombre de etapa]]"
responsable:
  - Persona o agente
```

No existe una entidad operativa separada llamada `iniciativa`. Cuando haga falta coordinar un resultado acotado, se representa mediante un módulo o una tarea principal, según su alcance.
