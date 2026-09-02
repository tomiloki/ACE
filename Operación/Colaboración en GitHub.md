---
tipo: metodología
estado: propuesta
actualizado: 2026-09-02
tarea: "[[T-025 - Definir metodología mínima de colaboración en GitHub]]"
---

# Colaboración en GitHub

## Propósito

Mantener `main` como la versión compartida y estable de ACE sin exigir una pull request por cada cambio pequeño.

## Ramas activas por frente

Cada integrante trabaja en una rama activa para el módulo o frente que tiene a cargo. No se crea una rama por cada tarea menor ni se mantienen ramas personales permanentes sin trabajo asociado.

La rama usa el formato `responsable/frente-resumen`, en minúsculas y con guiones: por ejemplo, `tomas/producto-evaluacion` o `matias/presentacion-duoc`.

La rama reúne los commits que construyen ese frente. Cuando se integra, puede eliminarse y su responsable abre otra rama cuando asuma un frente distinto.

## Cuándo usar `main`

Se puede trabajar y pushear directamente a `main` para cambios acotados que no formen parte de un módulo activo:

- tareas de backlog puntuales;
- borradores y antecedentes;
- correcciones documentales pequeñas;
- mantenimiento de archivos que ningún otro integrante esté editando.

Antes de pushear, el autor actualiza su copia de `main`, revisa el estado y el diff, y confirma que no existe trabajo concurrente sobre los mismos archivos. Los commits describen el cambio y enlazan la tarea cuando corresponda.

No se suben directamente a `main` cambios de código, configuración compartida, arquitectura, producto o un módulo en curso.

## Pull requests

Una pull request se abre al finalizar un módulo o cuando su resultado deba integrarse antes para habilitar otro frente. No es obligatoria para cada tarea interna del módulo.

La PR explica brevemente qué integra y enlaza el módulo, las tareas o el reporte que le dan contexto. Antes de abrirla, su autor actualiza la rama respecto de `main` y resuelve los conflictos que le correspondan.

El equipo revisa los cambios que afecten su trabajo. Tomás resuelve las decisiones de alcance y realiza el merge cuando la integración está lista. Si hay un conflicto que cambia una decisión compartida, se conversa antes de resolverlo; nadie sobrescribe trabajo ajeno ni hace force-push a `main`.

## Relación con ACE

Las tareas siguen definiendo el trabajo y los reportes conservan sus entregas y revisiones. Los commits y las PR aportan el historial técnico de cómo se integró ese trabajo; no sustituyen los artefactos operativos.

## Validación pendiente

La primera PR que cierre o integre un módulo servirá como prueba real de esta metodología. El equipo ajustará la guía solo si esa prueba revela una fricción concreta.
