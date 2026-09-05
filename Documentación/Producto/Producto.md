---
tipo: producto
estado: vigente
fecha: 2026-09-01
actualizado: 2026-09-04
---

# Producto

Problema, solución, alcance y objetivos confirmados en la Entrega 1 de Duoc. Este documento concentra la definición de producto aprobada durante T-017 y sirve de fuente para la documentación posterior. Los asuntos técnicos que declara pendientes se resuelven en sus tareas propias.

## Qué es ACE

Una plataforma de gestión de cartelería digital para Lumina Motion. Permite administrar de manera centralizada y remota las pantallas, el contenido y su programación en locaciones fijas. Ante un corte de internet, cada NUC continúa con los recursos que ya tiene programados localmente y se pueden realizar cambios desde la locación.

## Para quién

| Actor | Rol |
|---|---|
| Lumina Motion | Dueña de la plataforma. Estudio multimedia que instala y opera las pantallas. |
| Cristóbal | Jefe de informática de Lumina. Primer usuario, como administrador de todas las locaciones. |
| Operador | Acceso funcional desde la primera versión a las locaciones autorizadas, aunque Cristóbal sea el único usuario inicial. |

## Qué problema resuelve

La gestión de las pantallas de Lumina está descentralizada: utiliza herramientas y procedimientos separados, incluye cargas manuales de contenido y requiere intervención presencial. Esto dificulta el control conjunto de las pantallas y la coordinación de cambios, aumentando el tiempo operativo y el riesgo de errores.

## Solución

ACE busca centralizar la administración de pantallas, contenido y programación, permitiendo su gestión a distancia. Cuando un corte impide esa gestión remota, conserva la operación y permite cambios locales sobre los recursos programados y disponibles en la locación.

## Qué hace

Tres objetos principales:

| Objeto | Qué permite |
|---|---|
| Pantallas | Registrar dónde está cada pantalla y consultar la conectividad, última comunicación y estado de sincronización de su NUC. |
| Contenido | Mantener una biblioteca por locación y agrupar sus medios en playlists reutilizables dentro de esa locación. |
| Programación | Definir qué playlist se muestra, en qué destino y durante qué fechas, horarios y recurrencias. |

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

Desarrollar una plataforma de gestión de cartelería digital para Lumina Motion que permita administrar de manera centralizada y remota las pantallas, el contenido y su programación en locaciones fijas, manteniendo la reproducción con recursos programados localmente y permitiendo realizar cambios desde la locación cuando no exista conexión a internet.

### Objetivos específicos

1. Implementar la administración centralizada y remota de locaciones, sectores y pantallas, con acceso diferenciado para administradores y operadores según las locaciones autorizadas.
2. Desarrollar la gestión de contenido multimedia y playlists reutilizables, permitiendo organizar su orden, configurar tiempos de exhibición y limitar el acceso al contenido autorizado.
3. Implementar la programación de playlists por fechas, horarios y recurrencia semanal, con asignación a pantallas o sectores y sin solapamientos efectivos.
4. Habilitar la reproducción autónoma y la modificación local de contenido y programación sin internet, utilizando los recursos programados y disponibles localmente.
5. Incorporar la consulta del estado básico de conectividad de los NUC, incluyendo su última comunicación con la plataforma.
6. Validar el sistema en un entorno de pruebas con el cliente, verificando gestión remota, permisos y funcionamiento con y sin conexión a internet.

## Alcance inicial

Alcance de la primera versión de producto, confirmado en la Entrega 1 de Duoc. No implica entregar todo el software durante E-002, dedicada a la primera evaluación académica.

- Gestión centralizada y remota de locaciones, sectores y pantallas.
- Carga de medios MP4 H.264, JPG, PNG y GIF, reutilizables entre playlists de la misma locación, con orden, tiempos de exhibición y acceso limitado a las locaciones autorizadas.
- Programación por fechas, horarios y recurrencia semanal dirigida a un sector o a una pantalla, bloqueando solapamientos efectivos; una programación se puede editar, cancelar o interrumpir.
- Reproducción autónoma: el NUC conserva el contenido y la programación que le corresponden, y continúa reproduciendo los recursos programados localmente sin conexión.
- Cambios locales de contenido y programación sin internet, usando recursos disponibles localmente.
- Dos roles funcionales desde la primera versión: administrador y operador. El primer uso será por Cristóbal como administrador, sin requerir cuentas de operador al inicio.
- Consulta de conectividad, última comunicación y estado de sincronización de los NUC.

## Fuera de alcance

- Creación, edición o diseño del contenido. ACE lo distribuye, no lo produce.
- Mantenimiento físico de pantallas y cableado.
- Entidad cliente, suscripciones y personalización tipo SaaS, por ahora; no se impone una equivalencia entre cliente y locación.
- Permisos a nivel de sector.
- Monitoreo avanzado, más allá de la conectividad y última comunicación de los NUC.

## Restricción que define el producto

La reproducción y la intervención local deben seguir disponibles sin internet. Para ello, el NUC debe tener sincronizados con anticipación el contenido y la programación que le corresponden. Esto no implica conservar el acceso remoto durante un corte: los cambios requieren acceso desde la locación y recursos disponibles localmente; no se puede descargar contenido del servidor remoto sin conexión.

Estas capacidades no deciden todavía si el respaldo será individual por NUC o mediante un panel local conjunto. La alternativa sigue abierta en [[Gestión local sin internet]].

## Definiciones pendientes

- La definición aprobada y su cierre se registran en [[R-019 - Definición de producto y objetivos para la evaluación]].
- Topología de operación local: panel individual por NUC o PC conectado por LAN a varios NUC.
- Plataforma concreta del Player y validación de IndexedDB con contenido real.
- Segmentación y compartición de contenidos y playlists entre locaciones.
- Validación de las preguntas de operación y accesos con Cristóbal y el equipo.

## Enlaces

- [[Arquitectura]]
- [[Modelo de datos]]
- [[Clasificación del legacy]]
