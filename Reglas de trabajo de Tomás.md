
> Mapa vivo de preferencias. Todavía no es un harness formal.

## Comunicación

- Ser directo, breve y accionable.
- Reportar conclusiones, implicancias y siguiente paso.
- No trasladar al usuario todo el análisis interno.
- Entregar primero lo importante.
- Facilitar la comprensión cuando el tema sea complejo.

## Activación y orientación

- Tomás activa y enruta el trabajo. Los agentes no se activan entre sí.
- Antes de actuar, el agente puede leer y verificar el contexto, pero no modifica artefactos.
- El agente presenta siempre un reporte breve de iniciación en la conversación. No se guarda como documento.
- El reporte de iniciación indica: dónde estamos, qué cambió, qué decisiones o revisiones requieren atención y cómo recomienda proceder.
- Después del reporte de iniciación, el agente conversa alternativas e implicancias y promueve que el usuario tome las decisiones.
- La implementación requiere aprobación explícita posterior a esa conversación. Priorizar un frente o aprobar una idea no autoriza a ejecutarla.

## Decisiones

- Los agentes proponen; Tomás decide.
- No presentar hipótesis como hechos.
- Expresar incertidumbre cuando exista.
- Conversar antes de formalizar decisiones prematuras.
- No convertir automáticamente material heredado en verdad.

## Documentación

- Corto y rápido de leer por defecto.
- Explicar razones solo cuando sean importantes.
- Preferir Markdown para texto.
- Diagramar solamente cuando simplifique.
- Usar Mermaid mientras el resultado siga siendo legible; dividir o cambiar de formato cuando deje de serlo.
- Una instrucción explícita de Tomás puede justificar una excepción.
- Mantener una versión legible por IA.
- Los documentos finales muestran respuestas.
- Las preguntas quedan en conversación o se marcan como preliminares.

## Forma de avanzar

- Trabajar paso a paso y sin sobrecargar.
- Evitar estructura, plugins y procesos antes de necesitarlos.
- Priorizar fundamentos sobre velocidad aparente.
- Preparar una base sólida antes de publicar el repositorio.
- Dividir el trabajo sin esconder hallazgos transversales.

- Agregar reglas cuando aparezcan casos reales.
- Conversar y acordar cada regla nueva antes de adoptarla.

## Coordinación entre agentes

- El foco de cada agente vive en [[Registro de agentes ACE]]; este documento no lo repite.
- Todos pueden leer todo el vault.
- Antes de cambiar estructura, nombres o archivos que otro agente esté trabajando, se propone o reporta.
- Un archivo compartido tiene un solo editor a la vez.
- Los hallazgos transversales se reportan; no se corrigen silenciosamente.
- Si existe conflicto o desacuerdo, los agentes se detienen y Tomás decide.
- Un agente no revisa su propio trabajo.
- Los agentes revisores informan hallazgos; el ejecutor aplica los cambios.
- Si un cambio afecta el trabajo de otro agente, se actualizan la tarea y el reporte relacionados. Tomás activa al siguiente agente cuando corresponda.
