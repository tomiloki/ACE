---
tipo: reporte
estado: en_curso
revision_equipo: pendiente
modulo: "[[Producto y documentación para la primera evaluación]]"
tarea: "[[T-017 - Validar producto, alcance y objetivos para la evaluación]]"
fecha: 2026-09-03
---

# Definición de producto y objetivos para la evaluación

## Reporte del ejecutor

**Ejecutor:** Fenrir, en conversación con Tomás.

### Resumen

[[Producto]] reúne el problema, la solución, el alcance inicial y los objetivos acordados con Tomás. [[Borrador Fase 1]] recoge esa definición para el informe académico; [[Alcance inicial de ACE]] queda como antecedente incorporado, no como otra fuente que mantener.

La definición aborda gestión descentralizada, cargas manuales y dependencia presencial: propone administración centralizada y remota para locaciones fijas, sin perder reproducción ni cambios locales durante un corte de internet. Los operadores tendrán acceso funcional desde la primera versión, aunque Cristóbal sea el único usuario inicial. No se incorpora una entidad cliente ni un modelo SaaS por ahora.

El alcance describe el producto a construir, no una entrega completa de software en E-002. T-017 permanece abierta: esta consolidación no equivale a revisión de equipo ni validación del cliente.

### Evidencia y límites

- El problema, la solución, el objetivo general y los seis objetivos específicos coinciden entre Producto y el borrador académico.
- Las seis capacidades del borrador de alcance, sus exclusiones y sus precisiones pendientes están recogidas en Producto y sintetizadas en la descripción académica. Se explicitaron suscripciones, monitoreo avanzado y el límite temporal de E-002.
- La operación sin internet utiliza archivos disponibles localmente: no permite descargar del servidor remoto durante el corte ni conservar el acceso remoto sin conectividad.
- La verificación es documental; no se implementó ni probó software. Metodología, evidencias, planificación y Carta Gantt no fueron modificadas en esta consolidación.

### Asuntos abiertos y coherencia pendiente

- **Respaldo local:** sigue abierta la elección entre intervención por NUC y un panel cliente para varios NUC por red local. [[Gestión local sin internet]] conserva la consulta; no se ha decidido agregar un servidor local aparte.
- **Arquitectura preliminar:** [[Arquitectura]] todavía menciona «sitio del evento» y presenta una topología tentativa. Debe alinearse con locaciones fijas y distinguir la capacidad offline acordada de la alternativa técnica pendiente. Su tabla aún marca el motor de base de datos sin definir, pese a la elección de MariaDB conversada con Tomás; falta reflejar esa elección y distinguirla de la topología y persistencia local.
- **Factibilidad y planificación académicas:** conservan referencias a eventos, servidor local y opciones como SQLite/IndexedDB. No se ratificaron esas opciones mediante T-017; deben contrastarse con la arquitectura antes de presentar el informe. La planificación describe reproducción offline, pero debe comprobarse que también cubra la edición local y los permisos de operadores. Se señalan sin reescribir el trabajo de otros frentes.
- **Reglas de producto y datos:** faltan formatos admitidos, comportamiento de duración por tipo de medio, conflictos de programación y relaciones que hagan efectiva la segmentación de contenido y playlists. [[Modelo de datos]] y [[T-006 - Revisar modelo de datos con el equipo]] continúan su revisión propia. La necesidad futura de una entidad cliente sigue en [[Operadores, clientes y locaciones]].

## Revisión

**Pendiente — recomendación: equipo.** No se ha activado una revisión ni cerrado la tarea.

Revisar [[Producto]] y su incorporación en [[Borrador Fase 1]], y decidir si la definición sirve como base de la evaluación con los asuntos abiertos declarados. Las conclusiones y eventuales correcciones se registran en este mismo hilo. La conformidad conversacional de Tomás no se registra como una revisión final que todavía no se ha realizado.
