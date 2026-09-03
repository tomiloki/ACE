# ACE

Repositorio privado compartido para construir ACE y conservar en un mismo lugar su documentación, decisiones, diagramas, operación, código futuro y harnesses de agentes.

El repositorio representa el estado vigente del proyecto. La memoria de cada agente es auxiliar: ante una contradicción, prevalecen los archivos versionados aquí.

## Incorporarse al proyecto

### 1. Clonar

```bash
git clone https://github.com/tomiloki/ACE.git
cd ACE
```

La invitación de GitHub debe aceptarse antes de clonar el repositorio privado.

### 2. Abrir el workspace

Abre la carpeta clonada como vault de Obsidian. La documentación se conserva en Markdown y puede consultarse directamente desde el repositorio aunque Obsidian no esté abierto.

Los plugins y el estado personal de Obsidian no se comparten. Instala o configura herramientas locales solamente cuando el trabajo las necesite.

### 3. Orientarse

Humano y agente deben comenzar por:

1. [`AGENTS.md`](AGENTS.md): reglas operativas compartidas.
2. [`Ecosistema IA/Estado actual del ecosistema ACE.md`](Ecosistema%20IA/Estado%20actual%20del%20ecosistema%20ACE.md): situación vigente.
3. [`Ecosistema IA/Registro de agentes ACE.md`](Ecosistema%20IA/Registro%20de%20agentes%20ACE.md): identidad, etapa y foco de cada agente.
4. La etapa, el módulo de trabajo y la tarea activos enlazados desde esos documentos.

El agente presenta primero una orientación breve, conversa alternativas e implicancias con el humano y espera aprobación explícita antes de implementar.

### 4. Configurar el agente

- **Codex:** carga `AGENTS.md` desde la raíz del repositorio.
- **Claude Code:** `CLAUDE.md` importa el mismo núcleo.
- **Antigravity:** configura `.agents/rules/ace.md` como regla **Always On** del workspace.

Las identidades actuales son temporales. Si el agente no puede resolver inequívocamente quién es usando el registro y el contexto de la sesión, debe preguntárselo al humano antes de ejecutar.

## Forma de trabajo

- Las etapas orientan el tramo global del proyecto.
- Los módulos agrupan frentes de trabajo paralelizables.
- Las tareas dirigen el trabajo.
- Los reportes conservan entregas significativas y sus revisiones.
- La documentación registra conocimiento vigente.
- Los agentes proponen; los humanos deciden.
- No se versionan credenciales, secretos ni configuración local.

## Estructura del repositorio

- [`Documentación/`](Documentación): producto, arquitectura, modelo de datos y antecedentes académicos de Duoc.
- [`Ecosistema IA/`](Ecosistema%20IA): estado, etapas, registros y harnesses de agentes.
- [`Operación/`](Operación): módulos, tareas, reportes y reglas de trabajo.
- [`Borradores/`](Borradores): propuestas y material no canónico.
- [`Preguntas Equipo-Cliente/`](Preguntas%20Equipo-Cliente): dudas y alternativas para conversar con el equipo y/o el cliente, sin decisiones anticipadas.
- [`Legacy/`](Legacy): antecedentes históricos y validaciones iniciales.
- [`Excalidraw/`](Excalidraw): diagramas editables.

Consulta [`Operación/Sistema de reportaje ACE.md`](Operación/Sistema%20de%20reportaje%20ACE.md) antes de entregar o revisar trabajo.

## Estado

ACE está en la etapa **E-002 — Primera evaluación Duoc**. En este tramo el equipo debe completar, revisar, presentar y cerrar la primera evaluación usando la base operativa adoptada durante E-001.

El detalle vigente y el siguiente orden de trabajo viven en [`Ecosistema IA/Estado actual del ecosistema ACE.md`](Ecosistema%20IA/Estado%20actual%20del%20ecosistema%20ACE.md).
