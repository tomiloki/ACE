---
tipo: producto
estado: propuesta
fecha: 2026-09-01
---

# Producto

## Qué es ACE

Una plataforma de gestión de cartelería digital. Administra desde un solo lugar
las pantallas instaladas, el contenido que se reproduce en ellas y el horario
en que se reproduce.

## Para quién

| Actor | Rol |
|---|---|
| Lumina Motion | Dueña de la plataforma. Estudio multimedia que instala y opera las pantallas. |
| Cristóbal | Jefe de informática de Lumina. Primer usuario, como administrador de todas las locaciones. |
| Operador | Previsto para una incorporación posterior; gestiona las locaciones que tenga autorizadas. |

## Qué problema resuelve

Hoy la operación está fragmentada. Parte de las pantallas se carga a mano con
pendrive y el resto se maneja con software propietario de pago, sin un punto
único de control.

El costo aparece con los cambios de último momento: cada pantalla se atiende
por separado, consume tiempo del equipo técnico y expone la operación a errores
frente al público del cliente.

## Qué hace

Tres objetos y nada más:

| Objeto | Qué permite |
|---|---|
| Pantallas | Registrar dónde está cada pantalla y ver si está viva. |
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

## Alcance inicial

⟨PROPUESTA — requiere validación⟩

- Gestión de locaciones, sectores y pantallas.
- Carga de contenido reutilizable entre listas.
- Programación horaria dirigida a un sector o a una pantalla.
- Reproducción autónoma: la pantalla guarda el contenido y sigue funcionando
  sin conexión.
- Operación en sitio cuando se cae internet.
- Dos roles diseñados: administrador y operador. El primer uso será por Cristóbal como administrador, sin requerir operadores al inicio.

## Fuera de alcance

- Creación, edición o diseño del contenido. ACE lo distribuye, no lo produce.
- Mantenimiento físico de pantallas y cableado.
- Entidad cliente y personalización por cliente, por ahora; no se impone una equivalencia entre cliente y locación.
- Permisos a nivel de sector.

## Restricción que define el producto

La operación **no puede depender de internet**. Si la conexión se cae durante
una jornada, las pantallas siguen reproduciendo y el operador en sitio sigue
pudiendo cambiar lo que se muestra.

Esta restricción es la que separa a ACE de una herramienta de cartelería
convencional y la que condiciona la mayoría de las decisiones técnicas abiertas.

## Enlaces

- [[Arquitectura]]
- [[Modelo de datos]]
- [[Clasificación del legacy]]
