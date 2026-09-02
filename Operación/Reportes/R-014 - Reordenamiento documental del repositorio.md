---
tipo: reporte
estado: cerrado
revision_equipo: aprobada
modulo: transversal
tarea: "[[T-026 - Ordenar la estructura de carpetas del repositorio]]"
fecha: 2026-09-02
---

# Reordenamiento documental del repositorio

## Reporte del ejecutor

La documentación de producto quedó reunida en `Documentación/Producto/`: [[Producto]], [[Arquitectura]] y [[Modelo de datos]]. Los antecedentes de la primera evaluación se trasladaron a `Documentación/Duoc/`, por lo que `Duoc/` y `Decisiones/` ya no existen como carpetas independientes.

La raíz conserva solamente los puntos de entrada y la configuración compartida. El mapa de colaboración quedó en [[Mapa del ecosistema ACE]], las normas de operación en `Operación/`, y la prueba histórica de conexión en `Legacy/Validaciones iniciales/`.

El `README.md` ahora describe el propósito de cada espacio. Se actualizaron las referencias textuales a las rutas antiguas y los enlaces por nombre de Obsidian se conservan porque los archivos mantuvieron sus títulos.

## Verificación

- `git diff --check` no informó errores de espacio.
- No quedan referencias a `Decisiones/` ni a la antigua ubicación raíz de `Duoc/`.
- La carpeta `Decisiones/` se verificó vacía antes de eliminarla.
- La configuración local anidada `.obsidian/.obsidian/` no fue alterada; se añadió a `.gitignore` para impedir que su estado personal se versionara por accidente.

## Revisión

Tomás aprobó la estructura. `Excalidraw/` conservará su carpeta propia por ahora. Los criterios de aceptación de T-026 se consideran cumplidos y el reporte queda cerrado.

## Enlaces

- [[T-026 - Ordenar la estructura de carpetas del repositorio]]
- [[README]]
- [[Producto]]
- [[Arquitectura]]
- [[Modelo de datos]]
