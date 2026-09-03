---
tipo: producto
estado: propuesta
fecha: 2026-09-01
actualizado: 2026-09-03
---

# Producto

Problema, solución y objetivos acordados con Tomás durante T-017 el 2026-09-03. El alcance sigue en borrador y la tarea permanece abierta; esto no constituye validación final del cliente ni del equipo.

## Qué es ACE

Una plataforma de gestión de cartelería digital para Lumina Motion. Permite administrar de manera centralizada y remota las pantallas, el contenido y su programación en locaciones fijas.

## Para quién

| Actor | Rol |
|---|---|
| Lumina Motion | Dueña de la plataforma. Estudio multimedia que instala y opera las pantallas. |
| Cristóbal | Jefe de informática de Lumina. Primer usuario, como administrador de todas las locaciones. |
| Operador | Acceso funcional desde la primera versión a las locaciones autorizadas, aunque Cristóbal sea el único usuario inicial. |

## Qué problema resuelve

La gestión de las pantallas de Lumina está descentralizada: utiliza herramientas y procedimientos separados, incluye cargas manuales de contenido y requiere intervención presencial. Esto dificulta el control conjunto de las pantallas y la coordinación de cambios, aumentando el tiempo operativo y el riesgo de errores.

## Solución

ACE busca centralizar la administración de pantallas, contenido y programación, permitiendo su gestión a distancia y conservando la capacidad de operarlas y modificarlas localmente cuando no exista conexión a internet.

## Qué hace

Tres objetos y nada más:

| Objeto | Qué permite |
|---|---|
| Pantallas | Registrar dónde está cada pantalla y consultar la conectividad y última comunicación de su NUC. |
| Contenido | Subir un archivo una vez y agruparlo en listas reutilizables. |
| Programación | Decir qué lista se muestra, dónde y en qué horario. |

## Cómo se organiza

```
Locación
  └── Sector
        └── Pantalla
```

El permiso llega hasta la locación. Un operador puede tener una o varias locaciones asignadas; no se limita cada locación a un único operador. El sector solo sirve para dirigir contenido.

Para el alcance inicial no se modela una entidad cliente. Esto no equipara cliente con locación: la necesidad de incorporarlo se revisará con Cristóbal y el equipo en [[Operadores, clientes y locaciones]].

## Objetivos acordados

### Objetivo general

Desarrollar una plataforma de gestión de cartelería digital para Lumina Motion que permita administrar de manera centralizada y remota las pantallas, el contenido y su programación en locaciones fijas, manteniendo la reproducción y permitiendo realizar cambios localmente cuando no exista conexión a internet.

### Objetivos específicos

1. Implementar la administración centralizada y remota de locaciones, sectores y pantallas, con acceso diferenciado para administradores y operadores según las locaciones autorizadas.
2. Desarrollar la gestión de contenido multimedia y playlists reutilizables, permitiendo organizar su orden, configurar tiempos de exhibición y limitar el acceso al contenido autorizado.
3. Implementar la programación de playlists por fechas y horarios, con asignación a pantallas o sectores.
4. Habilitar la reproducción autónoma y la modificación local de contenido y programación sin internet, utilizando archivos disponibles en la locación.
5. Incorporar la consulta del estado básico de conectividad de los NUC, incluyendo su última comunicación con la plataforma.
6. Validar el sistema en un entorno de pruebas con el cliente, verificando gestión remota, permisos y funcionamiento con y sin conexión a internet.

## Alcance inicial

⟨PROPUESTA — requiere aprobación final⟩. El detalle para conversar permanece en [[Alcance inicial de ACE]].

- Gestión centralizada y remota de locaciones, sectores y pantallas.
- Carga de contenido reutilizable entre listas, con orden, tiempos de exhibición y acceso limitado a las locaciones autorizadas.
- Programación horaria dirigida a un sector o a una pantalla.
- Reproducción autónoma: la pantalla guarda el contenido y sigue funcionando
  sin conexión.
- Cambios locales de contenido y programación sin internet, usando archivos disponibles localmente.
- Dos roles funcionales desde la primera versión: administrador y operador. El primer uso será por Cristóbal como administrador, sin requerir cuentas de operador al inicio.
- Consulta de conectividad y última comunicación de los NUC.

## Fuera de alcance

- Creación, edición o diseño del contenido. ACE lo distribuye, no lo produce.
- Mantenimiento físico de pantallas y cableado.
- Entidad cliente y personalización por cliente, por ahora; no se impone una equivalencia entre cliente y locación.
- Permisos a nivel de sector.

## Restricción que define el producto

La reproducción y la intervención local deben seguir disponibles sin internet. Esto no implica conservar el acceso remoto durante un corte: los cambios requieren acceso desde la locación y archivos disponibles localmente; no se puede descargar contenido del servidor remoto sin conexión.

Estas capacidades no deciden todavía si el respaldo será individual por NUC o mediante un panel local conjunto. La alternativa sigue abierta en [[Gestión local sin internet]].

## Definiciones pendientes

- Aprobación final del alcance en [[Alcance inicial de ACE]].
- Formatos admitidos, reglas de duración y conflictos de programación.
- Segmentación y compartición de contenidos y playlists entre locaciones.
- Validación de las preguntas de operación y accesos con Cristóbal y el equipo.

## Enlaces

- [[Arquitectura]]
- [[Modelo de datos]]
- [[Clasificación del legacy]]
