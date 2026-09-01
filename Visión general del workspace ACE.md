# Visión general del workspace ACE

## Objetivo

Construir, paso a paso, un repositorio privado compartido para desarrollar ACE y conservar en un solo lugar:

- Código y configuración.
- Documentación y decisiones.
- Diagramas de arquitectura.
- Gestión del proyecto.
- Harnesses de IA: `AGENTS.md`, skills, agentes, plugins y convenciones.

La prioridad es que el entorno sea entendible, versionable y utilizable por todo el equipo, aunque cada persona use herramientas de IA diferentes.

## Equipo

| Persona | Alias | Herramientas actuales |
|---|---|---|
| Tomás Escalante | El Loki | Claude Code y Codex |
| Matías Salas | The Child | Gemini Pro y Antigravity |
| Paulo Loyola | The Wizard | Gemini Pro y Antigravity |

## Separación de responsabilidades

### GitHub: fuente de verdad operativa

- Código y ramas.
- Issues, tareas y planificación.
- Pull requests y revisiones.
- Historial de cambios y releases.

### Obsidian: fuente de conocimiento

- Documentación del proyecto.
- Decisiones técnicas y aprendizajes.
- Diagramas Excalidraw.
- Reuniones, investigación y enlaces entre conceptos.

No duplicar tareas completas en Obsidian y GitHub. Obsidian puede mostrar contexto o enlaces, pero la tarea oficial vive en GitHub.

## Principios

1. Avanzar por etapas pequeñas.
2. Instalar plugins solamente cuando resuelvan un problema real.
3. Preferir Markdown y estándares abiertos para evitar depender de una IA específica.
4. Versionar la configuración compartida, pero nunca credenciales ni secretos.
5. Revisar siempre los cambios realizados por IA.
6. Definir una única fuente de verdad para cada tipo de información.

## Plugins de Obsidian

### Ahora

- **Excalidraw**: instalado. Diagramas y arquitectura visual.
- **Obsidian Git**: instalado. Útil para sincronizar el vault cuando exista el repositorio; configurar con cuidado para evitar commits automáticos conflictivos.
- **Local REST API with MCP**: siguiente candidato. Conecta agentes con el vault y comenzará con permisos de solo lectura.

### Más adelante, cuando exista una necesidad concreta

- **Templater**: crear notas consistentes para decisiones, reuniones y documentación.
- **Dataview**: construir índices y paneles a partir de metadatos acordados.
- **QuickAdd**: automatizar capturas y creación de notas después de estabilizar las plantillas.
- **Advanced Tables**: comodidad opcional si el equipo usa muchas tablas Markdown.

### No instalar por ahora

- **Tasks, Kanban o TaskNotes**: duplicarían GitHub Issues/Projects.
- **Claudian o Copilot**: Tomás ya usa Claude Code y Codex, y el equipo emplea otros agentes. Primero conviene una integración neutral mediante archivos y MCP.
- **Remotely Save**: Git/GitHub será el mecanismo compartido; sumar otra sincronización aumenta el riesgo de conflictos.

## Estado actual

- Vault creado en `C:\PROYECTOS\A.C.E\ACE`.
- Excalidraw y Obsidian Git instalados.
- Git para Windows disponible.
- El directorio todavía no está inicializado como repositorio Git.
- Google Drive del proyecto continúa en modo de solo lectura hasta autorización explícita.

## Próximos pasos

1. Conectar Local REST API with MCP en modo de lectura.
2. Definir la estructura mínima del repositorio y del vault.
3. Crear el repositorio privado de GitHub y agregar al equipo.
4. Definir convenciones básicas antes de incorporar más plugins.
5. Evaluar Templater y Dataview cuando ya existan documentos reales.

