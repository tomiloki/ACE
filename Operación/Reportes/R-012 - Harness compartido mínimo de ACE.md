---
tipo: reporte
estado: cerrado
revision_humana: aprobada
modulo: "[[Operación y reportaje de ACE]]"
tarea: "[[T-013 - Definir harness compartido mínimo de ACE]]"
fecha: 2026-09-01
---

# Harness compartido mínimo de ACE

## Reporte del ejecutor

### Resumen

Se implementó un harness híbrido y compartido para Claude Code, Codex y Antigravity. `AGENTS.md` contiene el núcleo operativo universal; los adaptadores de plataforma lo cargan o referencian sin duplicar sus reglas. El contexto variable continúa en el vault y se recupera según la sesión y la tarea.

El núcleo establece identidad, recuperación, activación humana, aprobación explícita, comunicación, coordinación, persistencia y evolución de reglas. Las convenciones documentales no nucleares permanecen en [[Reglas de trabajo de Tomás]].

### Implicancias

- Codex puede cargar `AGENTS.md` directamente desde la raíz del repositorio.
- Claude Code carga `CLAUDE.md`, que importa `AGENTS.md`.
- Antigravity dispone de una regla de workspace que referencia el mismo núcleo.
- La identidad no se acopla a la plataforma: cada agente la conserva en su contexto persistente y la valida contra el registro.
- El vault se consulta como archivos Markdown; no se agregó integración REST con Obsidian.
- El contexto no se relee en cada mensaje: existe recuperación completa, recuperación por tarea y verificación breve previa a implementar.

### Detalle técnico y evidencia

- Núcleo: `AGENTS.md`.
- Tamaño inicial del núcleo: 4.496 caracteres, 691 palabras y 89 líneas; la medición real de tokens y adherencia queda para el piloto.
- Adaptador Claude Code: `CLAUDE.md` con `@AGENTS.md`.
- Adaptador Antigravity: `.agents/rules/ace.md` con `@../../AGENTS.md`.
- Fuente de identidad, etapa y foco: [[Registro de agentes ACE]].
- Punto de entrada al contexto variable: [[Estado actual del ecosistema ACE]].
- Sistema de entrega y revisión: [[Sistema de reportaje ACE]].

Se verificaron rutas, referencias y ausencia de reglas universales duplicadas en [[Reglas de trabajo de Tomás]]. No se ejecutó build porque la entrega modifica únicamente documentación e instrucciones.

### Abierto

- Configurar la regla de Antigravity como **Always On** desde la plataforma; la documentación oficial no expone metadatos de archivo para esa activación.
- Cada agente debe conservar su identidad en su propio contexto persistente; no se crearon credenciales locales compartidas.
- [[T-014 - Probar el harness compartido en una tarea real]] debe validar carga efectiva, recuperación, orientación y consumo de contexto en las plataformas disponibles.

### Ajuste posterior al piloto aislado

Los dos primeros turnos de T-014 confirmaron que el núcleo recupera el contexto, orienta antes de actuar y sostiene la conversación con el humano. También revelaron dos precisiones necesarias:

- La iniciación debe explicar en lenguaje humano qué intenta dejar resuelto la etapa, qué avances recientes construyeron la situación actual y por qué la tarea activa sigue de ellos. Los identificadores sirven como referencias, no reemplazan esa explicación, y no es necesario resumir el proyecto completo.
- La identidad persistente es preferente, pero no exclusiva: el agente puede inferirla mediante señales concordantes, incluido el humano asociado a la cuenta. Si la identidad no es inequívoca, debe preguntarla; no puede continuar anónimo.

Estos ajustes se incorporaron en `AGENTS.md` y luego fueron contrastados con el uso real de Atreus y Mímir desde Antigravity.

## Revisión

Tomás aprobó la revisión de equipo después de contrastar el núcleo con pruebas en Codex y Antigravity. Fenrir, Atreus y Mímir llegaron al mismo contexto operativo desde plataformas y usuarios distintos; Atreus y Mímir pudieron orientarse, conversar y aportar al repositorio sin instrucciones paralelas ni una segunda fuente de verdad.

El resultado se considera suficiente para cerrar T-013. El harness queda congelado por ahora y solo se reabrirá o ajustará ante fricciones reales y recurrentes.

## Enlaces

- [[AGENTS]]
- [[CLAUDE]]
- [[Reglas de trabajo de Tomás]]
- [[Estado actual del ecosistema ACE]]
- [[Registro de agentes ACE]]
- [[Sistema de reportaje ACE]]
- [[T-013 - Definir harness compartido mínimo de ACE]]
- [[T-014 - Probar el harness compartido en una tarea real]]
