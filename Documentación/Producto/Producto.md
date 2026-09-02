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
| Cristóbal | Jefe de informática de Lumina. Administra todos los sitios. |
| Operador del cliente | Opera las pantallas de su propio sitio. |

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
Sitio (el cliente)
  └── Sector
        └── Pantalla
```

El permiso llega hasta el sitio. El sector solo sirve para dirigir contenido.

## Alcance inicial

⟨PROPUESTA — requiere validación⟩

- Gestión de sitios, sectores y pantallas.
- Carga de contenido reutilizable entre listas.
- Programación horaria dirigida a un sector o a una pantalla.
- Reproducción autónoma: la pantalla guarda el contenido y sigue funcionando
  sin conexión.
- Operación en sitio cuando se cae internet.
- Dos roles: administrador y operador.

## Fuera de alcance

- Creación, edición o diseño del contenido. ACE lo distribuye, no lo produce.
- Mantenimiento físico de pantallas y cableado.
- Un cliente con más de un sitio.
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
