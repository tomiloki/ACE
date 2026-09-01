---
estado: borrador
fuente: diagrama Excalidraw 2026-08-31
actualizado: 2026-09-01
---

# Arquitectura

Refleja el diagrama. Componentes tentativos, decisiones sin cerrar.

## Topología

```mermaid
flowchart LR
  OP["PC Operador<br/>(remoto)"]
  API["Backend / API / BDD"]

  subgraph SITIO["Red local — sitio del evento"]
    SRV["Servidor interno (PC/NUC)<br/>+ frontend local"]
    PANT["Pantalla"]
  end

  OPS["Operador en sitio"]

  OP ==>|1 · principal · internet| API
  API ==> SRV
  SRV <==>|websockets| PANT
  OPS -->|2 · respaldo · sin internet| SRV
```

## Flujos

1. **Principal.** El operador remoto trabaja contra el backend por internet.
2. **Respaldo.** Si cae internet, la operación no puede depender del servidor
   remoto: el PC conectado a la pantalla expone su propio frontend y se opera
   en sitio.

Dónde corre el backend — nube, servidor interno, o ambos — está abierto.

## Componentes

| Componente | Estado |
|---|---|
| Pantalla | dibujado |
| Servidor interno (PC / NUC) | dibujado |
| PC Operador remoto | dibujado |
| Backend / API / BDD | dibujado, ubicación abierta |
| WebSockets | dibujado, funcionamiento abierto |
| Frontend local en el servidor interno | confirmado — respaldo sin internet |
| Electron en pantalla | opción sin evaluar |

## Abierto

| Caja | Nota |
|---|---|
| Modelo de datos | `Decisiones/` |
| Base de datos — motor y topología | `Decisiones/` |
| Lenguaje y framework backend | `Decisiones/` |
| Diseño de la API REST | `Decisiones/` |
| Diseño front-end | `Decisiones/` |
| Mockups | `Decisiones/` |
| Infraestructura y hosting | `Decisiones/` |
| Reproducción en pantalla | `Decisiones/` |
