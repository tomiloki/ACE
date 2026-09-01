---
tipo: clasificacion
estado: propuesta
fecha: 2026-09-01
---

# Clasificación del legacy

Material heredado recorrido contra las cajas del diagrama. Sin decisiones
técnicas. Nada se modificó ni se movió en Drive.

## Por caja del diagrama

### Modelo de datos

| Clasificación | Contenido |
|---|---|
| Útil | Diccionario de Datos: cuatro entidades con campos y tipos. |
| Útil | Convenciones: `uuid` en rutas de API, checksum SHA-256, hash de playlist, sufijo `_at`. |
| Contradicción | El Acta promete relación n-a-n entre contenido y pantallas; el Diccionario la modela 1-a-N. |
| Vacío | No existen usuarios ni roles. |
| Vacío | No existe jerarquía de ubicación; `groups` colapsa sitio y sector. |
| Descartable | `screens.zone` como texto libre. |

### Base de datos

| Clasificación | Contenido |
|---|---|
| Vacío | MariaDB aparece sin justificación en Acta, Visión y notas. |
| Vacío | No hay análisis de topología. El legacy asume una sola base remota. |
| Contradicción | El diagrama exige operación en sitio sin internet; el legacy no contempla datos locales. |

### Lenguaje y framework backend

| Clasificación | Contenido |
|---|---|
| Útil | Stack coherente en los tres documentos: Laravel 11, Filament v3, Spatie Media Library, Laravel Reverb. |
| Vacío | Ninguna justificación de la elección ni comparación con alternativas. |
| Descartable | Guía de Comandos y Terminal: material de aprendizaje de Laravel, no define el producto. |

### Diseño de la API REST

| Clasificación | Contenido |
|---|---|
| Útil | Patrón de respuesta: `metadata` con `server_time`, `playlist_hash` y `refresh_interval`, más la lista de medios. |
| Útil | Recomendaciones al cliente: no redescargar si el checksum coincide, seguir con la última playlist válida, ajustar el reloj con `server_time`. |
| Contradicción | La misma especificación usa `key` legible en el endpoint y `uuid` en su sección de seguridad. |
| Vacío | Sin autenticación. Los tokens quedan "para fases posteriores". |
| Vacío | No hay endpoint de heartbeat, pese a que el Acta promete telemetría de versión, uptime y almacenamiento. |
| Descartable | Base URL `karteleria.test`. |

### Diseño front-end

| Clasificación | Contenido |
|---|---|
| Útil | Filament v3 como panel de administración. |
| Vacío | Nada sobre el frontend local de respaldo que exige el diagrama. |
| Vacío | Las notas mencionan dos frontends, operador y superadmin; el Acta solo describe uno. |

### Mockups

| Clasificación | Contenido |
|---|---|
| Vacío | No existe ningún mockup en el material heredado. |

### Infraestructura y hosting

| Clasificación | Contenido |
|---|---|
| Vacío | El legacy no menciona hosting. Hostinger y Hostgator aparecen solo en el diagrama. |

### Reproducción en pantalla

| Clasificación | Contenido |
|---|---|
| Útil | Player web con caché en IndexedDB y descarga en segundo plano. |
| Útil | Formatos soportados: MP4, WebM, JPG, PNG, WebP y HTML. |
| Útil | Riesgo identificado: navegadores embebidos en Smart TV. |
| Contradicción | El Acta excluye firmware y sistemas operativos dedicados; el diagrama propone Electron, que es una aplicación de escritorio, no un navegador embebido. |
| Vacío | Se desconoce el hardware real de las pantallas. |

### Backend local

| Clasificación | Contenido |
|---|---|
| Vacío | El legacy asume un único servidor remoto. No cubre servidor interno ni operación en sitio. |

## Veredicto por documento

| Documento | Veredicto |
|---|---|
| Acta de Constitución | Rescatable. Entiende el producto. Corregir los hitos declarados como completados. |
| Documento de Visión | Rescatable. Buena definición del problema y del modelo Smart-Pull. |
| Matriz de Casos de Uso | Rescatable en parte. CU-01 a CU-05 siguen válidos; CU-06 cambia con la nueva jerarquía. |
| Diccionario de Datos | Insumo. Superado por la propuesta de modelo actual, pero aportó las convenciones. |
| Especificación Técnica de la API | Rescatable el patrón de respuesta. Descartar rutas y esquema de autenticación. |
| Guía de Comandos y Terminal | Descartable. Carpeta "Cosas puntuales". |
| A.C.E Notas Tomás | No es fuente de verdad. Aporta contexto de cliente no registrado en otro lugar. |

## Hallazgo

La copia de `A.C.E Notas Tomás` en Drive contiene información que **no está en
la copia local** del proyecto:

- Software que Lumina usa hoy: **Unreal Engine y Unity**.
- Cadena física: **pantallas → servidor → computador**.
- Menciona **paneles LED**, no solo pantallas.
- Tres preguntas adicionales para el cliente: si las pantallas son IOT o solo
  reproductores, si funcionan como módulos, y si se usan paneles LED.

## Resumen

| Clasificación | Cantidad |
|---|---:|
| Útil | 11 |
| Contradicción | 4 |
| Vacío | 13 |
| Descartable | 4 |

Las cajas **Mockups**, **Infraestructura** y **Backend local** no tienen
absolutamente nada aprovechable en el legacy.
