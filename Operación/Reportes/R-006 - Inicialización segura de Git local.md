---
tipo: reporte
estado: revisión
revision_humana: pendiente
iniciativa: "[[Operación y reportaje de ACE]]"
tarea: "[[T-007 - Preparar versionado local seguro]]"
fecha: 2026-09-01
---

# Inicialización segura de Git local

## Reporte del ejecutor

### Resumen

El vault ACE funciona como repositorio Git local sobre la rama `main`. El historial permite distinguir entregas, recuperar estados anteriores y coordinar cambios sin depender del estado actual de los archivos.

Se excluyen secretos, configuración local, plugins instalados y estado de ventana de Obsidian. El contenido y la configuración compartible permanecen versionados. No existe un remoto, por lo que la recuperación sigue limitada al equipo local.

### Implicancias

- Git aporta evidencia técnica y recuperación; no reemplaza tareas ni reportes.
- Los datos del plugin REST API quedan excluidos mediante `.obsidian/plugins/`.
- Markdown, CSS, JSON y YAML usan finales de línea LF.
- Sin remoto no hay publicación prematura, pero tampoco respaldo ante pérdida del equipo.

### Detalle técnico y evidencia

- Primer snapshot: `714e1d8 chore: initialize local ACE workspace`.
- Preparación local: `d4fa6fa chore: record local git setup`.
- `.gitignore` excluye estado local, plugins, `.env*`, claves, temporales y dependencias.
- `.gitattributes` normaliza los formatos de texto compartidos.
- Se verificó la rama `main` y la ausencia de remotos durante esta entrega.

### Abierto

- Definir remoto, política de ramas, respaldo y publicación cuando el equipo aborde GitHub.

## Revisión

Pendiente de Tomás. Debe confirmar que las exclusiones protegen el estado local y que continuar sin remoto sigue siendo adecuado para esta etapa.

## Enlaces

- [[T-007 - Preparar versionado local seguro]]
- [[Operación y reportaje de ACE]]
