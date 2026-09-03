---
caja: Modelo de datos
estado: propuesta
fecha: 2026-09-01
---

# Modelo de datos

```mermaid
classDiagram
  class sitios {
    +int id
    +string nombre
    +string direccion
    +bool activo
  }

  class sectores {
    +int id
    +int sitio_id
    +string nombre
    +string descripcion
  }

  class pantallas {
    +int id
    +int sector_id
    +uuid uuid
    +string nombre
    +enum estado
    +timestamp ultimo_latido_en
    +string ip_local
    +string version_player
    +string resolucion
    +bool activa
  }

  class medios {
    +int id
    +string nombre_archivo
    +string ruta
    +enum tipo
    +string checksum
    +int duracion
    +int tamano
    +int subido_por
  }

  class playlists {
    +int id
    +string nombre
    +string hash
    +bool activa
  }

  class playlist_items {
    +int id
    +int playlist_id
    +int medio_id
    +int orden
  }

  class programaciones {
    +int id
    +int playlist_id
    +int sector_id
    +int pantalla_id
    +time hora_inicio
    +time hora_fin
    +date fecha_inicio
    +date fecha_fin
    +bool activa
  }

  class usuarios {
    +int id
    +string nombre
    +string email
    +string password_hash
    +enum rol
    +int sitio_id
    +bool activo
  }

  sitios "1" --> "*" sectores
  sitios "1" --> "*" usuarios
  sectores "1" --> "*" pantallas
  sectores "1" --> "*" programaciones
  pantallas "1" --> "*" programaciones
  playlists "1" --> "*" playlist_items
  playlists "1" --> "*" programaciones
  medios "1" --> "*" playlist_items
  usuarios "1" --> "*" medios
```

## Entidades

| Entidad | Qué es |
|---|---|
| `sitios` | Instalación fija. Equivale al cliente de Lumina. |
| `sectores` | Subdivisión del sitio: Lobby, Zona VIP. |
| `pantallas` | Dispositivo físico. Pertenece a un sector. |
| `medios` | Archivo único, con checksum. |
| `playlists` | Lista ordenada de contenido. |
| `playlist_items` | Un medio dentro de una playlist, con su orden. |
| `programaciones` | Qué playlist se emite, dónde y en qué ventana horaria. |
| `usuarios` | Acceso a nivel de sitio. |

## Campos que merecen explicación

- `pantallas.uuid` — identificador usado en la API. Evita exponer el `id`
  incremental y que se puedan adivinar otras pantallas. Viene del legacy.
- `playlists.hash` — cambia cada vez que se edita la lista. La pantalla lo
  compara y sabe si hay novedades sin descargar el contenido completo.
  Viene del legacy.
- `medios.checksum` — SHA-256 del archivo. La pantalla no vuelve a descargar
  lo que ya tiene. Viene del legacy.
- `programaciones.sector_id` y `pantalla_id` — se usa uno u otro. Si ambos
  van vacíos, la programación es global.
- `usuarios.sitio_id` — vacío en el administrador, que ve todos los sitios.

## Decidido

- **No existe entidad evento.** Las pantallas quedan instaladas de forma fija.
  El horario cuelga del contenido, no de una jornada.
- **Jerarquía de dos niveles:** sitio → sector → pantalla.
- **Cliente = sitio.** Un cliente no tiene más de un sitio por ahora.
- **Permisos a nivel de sitio.** El sector dirige contenido, no controla acceso.
- **Dos roles:** administrador (todos los sitios) y operador (su sitio).
- **El archivo se separa de su uso.** Un medio se reusa en varias playlists sin
  volver a subirlo.
- **La playlist no lleva horario ni destino.** Eso vive en `programaciones`.

## Convenciones

- Tablas en plural y `snake_case`.
- Nombres en español.
- Las claves foráneas terminan en `_id`.
- Los campos de fecha y hora de un evento terminan en `_en`.

## Descartado del legacy

- `groups` plano: colapsaba sitio y sector en una sola tabla.
- `media_items.playlist_id`: ataba cada archivo a una única playlist.
- Horario y destino dentro de `playlists`: tres responsabilidades en una tabla.
- `screens.zone` como texto libre: lo reemplaza `sectores`.

## Abierto

- ¿Se puede sobrescribir la duración de una imagen dentro de una playlist, o
  la duración es siempre la del medio?
- ¿Qué pasa si dos programaciones se superponen en la misma pantalla? Hace
  falta una regla: prioridad, o prohibir el solapamiento.
- ¿Las programaciones se repiten por día de la semana, o solo por rango de
  fechas?
- Permisos por sector (Cristóbal lo ve improbable).


NOTAS EQUIPO 

-Relacion sitios usuarios- un usuario deberia poder tener varioas sitios
-un medio tiene un nduracion, pero no necesariamente , podria ser ffoto, gif , etc; el medio tienen  qu ete ner un duracion dentro de la reproduccion y hay que fijar de en qu etabla vive eso(programacion,playlist,playlistitem)