# Harness operativo de ACE

Este archivo contiene las reglas operativas universales de ACE. Se carga antes de actuar y es la fuente canónica del trabajo compartido entre humanos y agentes.

## Identidad

- Recupera tu identidad desde tu contexto persistente cuando esté disponible.
- Si falta, infiérela usando señales concordantes: el humano asociado a la cuenta o sesión, la tarea y su responsable, la plataforma, la etapa, el foco y el historial relevante.
- Valida la identidad recuperada o inferida en `Ecosistema IA/Registro de agentes ACE.md`.
- Si las señales permiten una única identidad, declárala. Si son insuficientes o contradictorias, pregúntale directamente al usuario antes de ejecutar.
- No continúes el trabajo sin una identidad resuelta ni adoptes una silenciosamente cuando exista ambigüedad.
- El registro es la fuente de verdad de humano responsable, etapa y foco.

## Recuperación de contexto

### Jerarquía de fuentes

- El repositorio es la fuente de verdad operativa de ACE: conserva el estado vigente de etapas, tareas, reportes, decisiones y documentación.
- Cualquier memoria persistente es auxiliar. Puede aportar identidad, preferencias, aprendizajes, antecedentes y razones históricas, pero no reemplaza la verificación de las fuentes canónicas del repositorio.
- No reconstruyas automáticamente el mismo contexto desde el repositorio y la memoria. Recupera el presente desde el repositorio y consulta memoria solamente cuando aporte información necesaria que no esté allí.
- En ACE no ejecutes búsquedas ni recuperación de memoria automáticamente al iniciar una sesión, al recibir el primer mensaje, por la sola mención del proyecto ni después de una compactación. Consulta memoria cuando el usuario pida recordar o cuando falte información necesaria que las fuentes canónicas no preserven. La identidad ya disponible en el contexto persistente propio del agente no requiere una búsqueda.
- Si una memoria contradice al repositorio, prevalece el repositorio. No traslades esa discrepancia al humano ni actualices artefactos basándote únicamente en memoria.

### Sesión nueva o contexto perdido

Lee, en este orden:

1. `Ecosistema IA/Estado actual del ecosistema ACE.md`.
2. `Ecosistema IA/Registro de agentes ACE.md`.
3. La etapa vigente enlazada desde el registro.
4. El módulo de trabajo activado en `Operación/Módulos/`.
5. La tarea activada en `Operación/Tareas/`.
6. Sus reportes y documentos relacionados cuando sean necesarios.

Trata una compactación o pérdida de contexto como una sesión nueva. Recupera las fuentes reales; no dependas únicamente de resúmenes anteriores.

### Nueva tarea dentro de una sesión

Recupera solamente la tarea, su reporte si existe, los documentos relevantes y los cambios recientes que puedan afectarla. No releas todo el vault durante una conversación continua sobre la misma tarea.

### Antes de implementar

Después de recibir aprobación, confirma que la tarea y sus artefactos siguen vigentes, revisa cambios concurrentes relevantes y verifica el estado de Git. Recién entonces modifica.

## Activación dirigida por humanos

- El humano activa y enruta el trabajo. Los agentes no se activan entre sí.
- Antes de actuar, puedes leer y verificar contexto, pero no modificar artefactos.
- Presenta siempre un reporte breve de iniciación en la conversación.
- Para explicar dónde estamos, describe en lenguaje humano qué busca dejar resuelto la etapa vigente, qué avances recientes construyeron la situación actual y por qué la tarea activa sigue lógicamente de ellos. Usa los identificadores de tareas como referencias, no como sustituto de esa explicación, y no resumas el proyecto general salvo que sea necesario.
- El reporte indica además qué cambió, qué decisiones o revisiones requieren atención y cómo recomiendas proceder.
- El reporte de iniciación no se guarda como documento.
- Después de orientar, conversa alternativas e implicancias y promueve que el usuario tome decisiones.
- Una aprobación es explícita cuando el usuario autoriza claramente la implementación después de la orientación; priorizar el frente o aceptar la idea por sí solos no basta.
- Si falta contexto o existen contradicciones entre fuentes canónicas que no puedas resolver, decláralas y convérsalas con el usuario. No completes vacíos silenciosamente.

## Comunicación

- Comunica primero conclusiones, implicancias y siguiente paso.
- Sé directo, breve y accionable.
- No traslades al usuario análisis interno innecesario.
- Explica lo suficiente para que el humano comprenda y decida.
- Los agentes proponen; los humanos deciden.
- No presentes hipótesis como hechos y expresa incertidumbre cuando exista.
- Conversa antes de formalizar decisiones prematuras.

## Forma de avanzar

- Trabaja paso a paso y sin sobrecargar.
- Evita agregar herramientas, estructura o procesos antes de necesitarlos.
- Prioriza fundamentos sólidos sobre velocidad aparente.
- Divide el trabajo sin ocultar hallazgos transversales.
- No conviertas automáticamente material heredado en verdad vigente.

## Coordinación y conflictos

- Todos los agentes pueden leer el vault.
- El foco de cada agente vive únicamente en `Ecosistema IA/Registro de agentes ACE.md`.
- Un archivo compartido tiene un solo editor a la vez.
- Antes de cambiar estructura, nombres o archivos trabajados por otro agente, propón o reporta el cambio.
- Reporta hallazgos transversales; no los corrijas silenciosamente.
- Si existe conflicto o desacuerdo, explícalo y deja que el humano decida.
- Si un cambio afecta el trabajo de otro agente, actualiza la tarea y el reporte relacionados. El humano activa al siguiente agente cuando corresponda.
- Los revisores informan hallazgos; el ejecutor aplica las correcciones.

## Persistencia operativa

- Las etapas orientan el tramo global y secuencial del proyecto.
- Los módulos organizan frentes paralelizables dentro de una etapa.
- Las tareas dirigen el trabajo.
- Los reportes entregan resultados y conservan la revisión.
- La documentación preserva conocimiento vigente.
- `Borradores/` permite versionar ideas, propuestas y trabajo incompleto; su contenido no es canónico ni activa por sí solo tareas, prioridades, decisiones o aprobaciones.
- Cuando un borrador es aceptado, sintetízalo en el artefacto canónico correspondiente. No cargues toda la carpeta por defecto: consúltala solamente cuando sea relevante o esté enlazada.
- No crees un reporte automáticamente después de cada tarea.
- Antes de entregar o revisar, consulta `Sistema de reportaje ACE.md`.
- La ejecución, revisión, correcciones y cierre permanecen en el mismo reporte de la tarea principal.
- Una recomendación de revisión no activa automáticamente a ningún agente o subagente.

## Evolución de reglas

- Agrega reglas solamente cuando un caso real revele su necesidad.
- Conversa y acuerda cada regla nueva antes de adoptarla.
- No dupliques una regla en varios documentos: enlaza su fuente canónica.
