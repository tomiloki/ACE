---
tipo: reporte
estado: abierto
tarea: "[[T-020 - Construir plan de trabajo y Carta Gantt]]"
modulo: "[[Planificación y factibilidad]]"
responsable:
  - Matías
  - Atreus
revision: equipo
resultado_revision: pendiente
fecha: 2026-09-02
---

# Plan de trabajo y Carta Gantt para las 18 semanas de ACE

## Reporte del ejecutor (Matías / Atreus)

### Resumen

Se construyó el **Plan de Trabajo detallado** y la **Carta Gantt de 18 semanas** para el proyecto ACE (Capstone PTY4614), cumpliendo con los criterios de evaluación de los **Indicadores 7 y 12** de la pauta de Duoc UC (20 puntos grupales).

El plan organiza las 18 semanas académicas (10 de agosto al 12 de diciembre de 2026) en 6 fases secuenciales, articulando las 3 competencias del perfil de egreso de Ingeniería en Informática con 21 actividades concretas, recursos asignados, responsabilidades específicas para Tomás, Matías y Paulo, y la alineación estricta a los 4 hitos evaluados por Duoc.

---

## 1. Plan de Trabajo por Competencias (Indicador 7 Duoc)

A continuación se detalla la matriz de actividades según la estructura exigida por la pauta de Duoc UC:

| Competencia del Perfil de Egreso | Nombre de la Actividad | Descripción | Recursos Requeridos | Duración | Responsable | Observaciones / Entregables |
|---|---|---|---|:---:|---|---|
| **C3.** Aplicar principios de ingeniería de software y especificación formal de requerimientos. | **1.1** Levantamiento de problemática y requerimientos | Reuniones con Cristóbal (Lumina Motion) para relevar dolores operativos en pantallas y eventos. | Canal de comunicación, minutas de reunión | S1 - S2 (2 sem) | Matías Salas | Requerimientos funcionales y no funcionales base. |
| **C3.** Aplicar principios de ingeniería de software y especificación formal de requerimientos. | **1.2** Definición de alcance y análisis de factibilidad | Delimitación del MVP, objetivos generales/específicos y factibilidad técnica/operativa. | Documentación técnica, repositorio | S2 - S3 (2 sem) | Tomás Escalante, Matías Salas | Declaración de alcance y factibilidad. |
| **C1.** Diseñar, desarrollar e integrar soluciones de software cliente-servidor y distribuidas. | **1.3** Selección de stack y arquitectura distribuida | Definición de arquitectura centralizada y clientes de pantalla con soporte offline. | Herramientas de diagramado, benchmarks | S2 - S3 (2 sem) | Tomás Escalante, Paulo Loyola | Diagrama de arquitectura y stack tecnológico. |
| **C3.** Aplicar principios de ingeniería de software y especificación formal de requerimientos. | **1.4** Elaboración de Informe y Presentación Fase 1 | Redacción formal del informe de definición y armado de diapositivas de defensa. | Plantilla oficial Duoc, Google Slides / PDF | S3 - S4 (2 sem) | Equipo (Tomás, Matías, Paulo) | **Hito Evaluado S4:** Presentación Grupal Fase 1. |
| **C3.** Aplicar principios de ingeniería de software y especificación formal de requerimientos. | **2.1** Ajustes post-retroalimentación Fase 1 | Incorporación de observaciones del docente al diseño y cronograma del proyecto. | Pauta y rúbrica docente | S5 (1 sem) | Equipo | Requerimientos refinados. |
| **C2.** Modelar, consultar y administrar bases de datos relacionales y almacenamiento local. | **2.2** Modelado de datos relacional y local | Diseño del esquema de base de datos (sitios, pantallas, medios, playlist, programación). | Motor DB, herramientas CASE, SQL | S5 - S6 (2 sem) | Paulo Loyola, Tomás Escalante | Diagrama Entidad-Relación y script DDL. |
| **C1.** Diseñar, desarrollar e integrar soluciones de software cliente-servidor y distribuidas. | **2.3** Diseño UI/UX del Panel de Administración | Elaboración de wireframes y flujos interactivos para gestión de pantallas y programación. | Figma / wireframing | S5 - S6 (2 sem) | Paulo Loyola | Prototipo de interfaz de usuario. |
| **C1.** Diseñar, desarrollar e integrar soluciones de software cliente-servidor y distribuidas. | **2.4** Especificación de contratos de API RESTful | Definición de endpoints, payloads JSON y protocolos de autenticación y telemetría. | OpenAPI / Swagger, Postman | S6 (1 sem) | Tomás Escalante | Documentación técnica de APIs. |
| **C2.** Modelar, consultar y administrar bases de datos relacionales y almacenamiento local. | **3.1** Implementación de base de datos y persistencia | Despliegue de base de datos central y configuración de ORM / capa de acceso a datos. | Servidor DB, ORM (Node/Python) | S7 - S8 (2 sem) | Paulo Loyola, Tomás Escalante | Base de datos operativa y migraciones. |
| **C1.** Diseñar, desarrollar e integrar soluciones de software cliente-servidor y distribuidas. | **3.2** Desarrollo de Backend Core y API REST | Construcción de endpoints para carga de medios, control de pantallas y autenticación. | Framework Backend (FastAPI / Express), Git | S7 - S9 (3 sem) | Tomás Escalante | Servicios backend funcionales. |
| **C1.** Diseñar, desarrollar e integrar soluciones de software cliente-servidor y distribuidas. | **3.3** Desarrollo de Frontend Admin Web | Construcción de interfaz web reactiva para administración de pantallas y contenido. | Framework Frontend (React / Vue), Node.js | S8 - S10 (3 sem) | Paulo Loyola | Panel de control web operativo. |
| **C1.** Diseñar, desarrollar e integrar soluciones de software cliente-servidor y distribuidas. | **3.4** Construcción del Player Multimedia base | Desarrollo del reproductor en pantalla para ejecución de listas de medios locales. | Electron / Web Player, HTML5 Canvas/Video | S8 - S10 (3 sem) | Matías Salas, Tomás Escalante | Reproductor base ejecutando video/imagen. |
| **C3.** Aplicar principios de ingeniería de software y especificación formal de requerimientos. | **3.5** Integración de avance y validación intermedia | Pruebas integradas de flujo completo y validación de avance con Lumina Motion. | Entorno de pruebas, servidor local | S9 - S10 (2 sem) | Matías Salas, Equipo | **Hito Evaluado S10:** Entrega de Avance (Evaluada). |
| **C3.** Aplicar principios de ingeniería de software y especificación formal de requerimientos. | **3.6** Revisión de retroalimentación S10 | Evaluación del feedback docente de la entrega de avance y priorización de sprints finales. | Rúbrica y observaciones | S11 (1 sem) | Equipo | Plan de sprints finales ajustado. |
| **C1.** Diseñar, desarrollar e integrar soluciones de software cliente-servidor y distribuidas. | **4.1** Lógica de programación horaria avanzada | Algoritmos de calendarización por horario, días de semana, sectores y prioridades. | Algoritmos de scheduler, Backend | S12 - S13 (2 sem) | Paulo Loyola, Tomás Escalante | Motor de programación horaria integrado. |
| **C1 / C2.** Persistencia y resiliencia offline. | **4.2** Resiliencia offline y almacenamiento local | Almacenamiento local en Player (caché de medios) para reproducción continua sin internet. | SQLite / IndexedDB, caché local | S12 - S14 (3 sem) | Tomás Escalante, Matías Salas | Player autónomo frente a cortes de red. |
| **C1.** Diseñar, desarrollar e integrar soluciones de software cliente-servidor y distribuidas. | **4.3** Sincronización y telemetría de pantallas | Comunicación bidireccional: descarga de contenidos y reporte de estado (heartbeat). | WebSockets / Polling, Telemetría | S13 - S14 (2 sem) | Tomás Escalante, Paulo Loyola | Sincronización en vivo y monitoreo de salud. |
| **C3.** Aplicar principios de ingeniería de software y especificación formal de requerimientos. | **4.4** Pruebas integrales de tolerancia a fallos | Pruebas de simulación de cortes de energía, desconexión de red y recuperación automática. | Banco de pruebas, switches de red | S14 (1 sem) | Matías Salas, Equipo | Informe de pruebas de resiliencia. |
| **C1.** Diseñar, desarrollar e integrar soluciones de software cliente-servidor y distribuidas. | **5.1** Despliegue en Staging y pruebas con hardware real | Configuración de servidor en la nube/sitio e instalación en pantallas físicas de prueba. | Servidor Cloud / Mini PC de pantalla | S15 (1 sem) | Matías Salas, Tomás Escalante | Sistema desplegado en entorno productivo. |
| **C3.** Aplicar principios de ingeniería de software y especificación formal de requerimientos. | **5.2** Consolidación de Informe Final y Manuales | Redacción de manual de usuario, manual técnico y memoria final del proyecto. | Plantilla oficial Duoc, Repositorio | S15 (1 sem) | Paulo Loyola, Equipo | **Hito Evaluado S15:** Entrega Final de Proyecto. |
| **C3.** Aplicar principios de ingeniería de software y especificación formal de requerimientos. | **6.1** Validación de aceptación y defensa final | Pruebas de aceptación con cliente (Lumina Motion), preparación de guion y examen de título. | Diapositivas, prototipo en vivo, video demo | S16 - S18 (3 sem) | Equipo (Tomás, Matías, Paulo) | **Hito Evaluado S17-S18:** Examen y Presentación Final. |

---

## 2. Carta Gantt — 18 Semanas (Indicador 12 Duoc)

Alineada con el calendario académico oficial del segundo semestre 2026:

| # | Actividad | Resp. | S1<br><sub>10-15 ago</sub> | S2<br><sub>17-22 ago</sub> | S3<br><sub>24-29 ago</sub> | S4<br><sub>31-05 sep</sub><br>**[H1]** | S5<br><sub>07-12 sep</sub> | S6<br><sub>14-19 sep</sub> | S7<br><sub>21-26 sep</sub> | S8<br><sub>28-03 oct</sub> | S9<br><sub>05-10 oct</sub> | S10<br><sub>12-17 oct</sub><br>**[H2]** | S11<br><sub>19-24 oct</sub> | S12<br><sub>26-31 oct</sub> | S13<br><sub>02-07 nov</sub> | S14<br><sub>09-14 nov</sub> | S15<br><sub>16-21 nov</sub><br>**[H3]** | S16<br><sub>23-28 nov</sub> | S17<br><sub>30-05 dic</sub><br>**[H4]** | S18<br><sub>07-12 dic</sub><br>**[H4]** |
|---|---|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **1.1** | Levantamiento requerimientos Lumina | Matías | █ | █ | | | | | | | | | | | | | | | | |
| **1.2** | Definición alcance y factibilidad | Tomás/Matías | | █ | █ | | | | | | | | | | | | | | | |
| **1.3** | Stack y arquitectura distribuida | Tomás/Paulo | | █ | █ | | | | | | | | | | | | | | | |
| **1.4** | Informe y Diapositivas Fase 1 | Equipo | | | █ | █ | | | | | | | | | | | | | | |
| **★** | **Hito 1: Presentación Grupal Fase 1** | **Equipo** | | | | **◆** | | | | | | | | | | | | | | |
| **2.1** | Ajustes post-retroalimentación S4 | Equipo | | | | | █ | | | | | | | | | | | | | |
| **2.2** | Modelo de datos relacional y local | Paulo/Tomás | | | | | █ | █ | | | | | | | | | | | | |
| **2.3** | Diseño UI/UX Panel Administración | Paulo | | | | | █ | █ | | | | | | | | | | | | |
| **2.4** | Especificación de APIs RESTful | Tomás | | | | | | █ | | | | | | | | | | | | |
| **3.1** | Implementación BD y persistencia | Paulo/Tomás | | | | | | | █ | █ | | | | | | | | | | |
| **3.2** | Desarrollo Backend Core y API | Tomás | | | | | | | █ | █ | █ | | | | | | | | | |
| **3.3** | Desarrollo Frontend Admin Web | Paulo | | | | | | | | █ | █ | █ | | | | | | | | |
| **3.4** | Construcción Player Multimedia base | Matías/Tomás | | | | | | | | █ | █ | █ | | | | | | | | |
| **3.5** | Integración y validación avance | Matías/Equipo| | | | | | | | | █ | █ | | | | | | | | |
| **★** | **Hito 2: Entrega Avance de Proyecto** | **Equipo** | | | | | | | | | | **◆** | | | | | | | | |
| **3.6** | Revisión feedback intermedio S10 | Equipo | | | | | | | | | | | █ | | | | | | | |
| **4.1** | Lógica de programación horaria | Paulo/Tomás | | | | | | | | | | | | █ | █ | | | | | |
| **4.2** | Resiliencia offline y Player local | Tomás/Matías | | | | | | | | | | | | █ | █ | █ | | | | |
| **4.3** | Sincronización y telemetría | Tomás/Paulo | | | | | | | | | | | | | █ | █ | | | | |
| **4.4** | Pruebas integrales de tolerancia | Matías/Equipo| | | | | | | | | | | | | | █ | | | | |
| **5.1** | Despliegue Staging y hardware real | Matías/Tomás | | | | | | | | | | | | | | | █ | | | |
| **5.2** | Consolidación Informe Final | Paulo/Equipo | | | | | | | | | | | | | | | █ | | | |
| **★** | **Hito 3: Entrega Final de Proyecto** | **Equipo** | | | | | | | | | | | | | | | **◆** | | | |
| **6.1** | Validación Lumina y Ajustes Finales | Matías/Equipo| | | | | | | | | | | | | | | | █ | █ | |
| **6.2** | Preparación Examen y Video Demo | Paulo/Matías | | | | | | | | | | | | | | | | | █ | █ |
| **★** | **Hito 4: Examen / Presentación Final**| **Equipo** | | | | | | | | | | | | | | | | | | **◆** | **◆** |

---

## 3. Factibilidad: Facilitadores y Obstaculizadores (Indicador 4 Duoc)

### Facilitadores
1. **Acceso directo al cliente:** Comunicación continua con Cristóbal, jefe del área de informática de Lumina Motion, asegurando retroalimentación directa sobre el dolor operativo real.
2. **Harness y base operativa con IA:** Adopción de una metodología asistida por IA (ACE) versionada en Git, optimizando la trazabilidad, documentación técnica y velocidad de desarrollo.
3. **Roles y especialidades complementarias:** División clara de responsabilidades: Tomás (Backend y Arquitectura), Paulo (Frontend y Bases de Datos) y Matías (Gestión, Player y Validación con Cliente).

### Obstaculizadores y Estrategias de Mitigación
1. **Fallas o heterogeneidad en el hardware de pantallas:**
   - *Riesgo:* Distintas resoluciones, sistemas operativos o capacidades gráficas en los sitios de Lumina Motion.
   - *Mitigación:* Desarrollo del Player sobre tecnologías web estándar (HTML5/Canvas) y empaquetado multiplataforma liviano, testeado en hardware acotado y validado en la Semana 15.
2. **Interrupción prolongada de conexión a internet en locales/eventos:**
   - *Riesgo:* Incapacidad de actualizar contenidos o pantallas en negro ante cortes de red.
   - *Mitigación:* Arquitectura con caché local persistente (reproducción en bucle autónomo) y sincronización asíncrona solo cuando se restablece la red.
3. **Tiempos ajustados de desarrollo (18 semanas):**
   - *Riesgo:* Retrasos en la entrega final debido a sobrecarga de requerimientos.
   - *Mitigación:* Priorización estricta de un MVP funcional para la Semana 10 (Hito 2) y foco posterior exclusivo en resiliencia offline.

---

## Próximos Pasos y Enlaces

1. Volcar esta matriz en el archivo canónico [Borrador Fase 1.md](file:///c:/Users/matni/.gemini/antigravity/scratch/ACE/Documentaci%C3%B3n/Duoc/Borrador%20Fase%201.md) para que Paulo/Mímir lo integren al informe final ([T-021](file:///c:/Users/matni/.gemini/antigravity/scratch/ACE/Operaci%C3%B3n/Tareas/T-021%20-%20Completar%20y%20consolidar%20el%20informe%20final.md)).
2. Utilizar esta estructura como insumo directo para diseñar las diapositivas de la presentación grupal ([T-022](file:///c:/Users/matni/.gemini/antigravity/scratch/ACE/Operaci%C3%B3n/Tareas/T-022%20-%20Dise%C3%B1ar%20narrativa%20y%20diapositivas.md)).

- [[T-020 - Construir plan de trabajo y Carta Gantt]]
- [[Borrador Fase 1]]
- [[E-002 - Primera evaluación Duoc]]
