---
tipo: borrador
estado: propuesta
fase: 1
fecha_limite: 2026-09-05
fecha: 2026-09-01
actualizado: 2026-09-03
---

# Borrador Fase 1 Duoc

Sigue la estructura de `1.5_GuiaEstudiante_Fase 1_Definicion Proyecto APT.docx`.

Los campos marcados **⟨PENDIENTE⟩** requieren respuesta del equipo y no se
completaron por suposición. Los marcados **⟨PROPUESTA⟩** son redacción sugerida
que Tomás debe validar antes de usarse.

En T-017, Tomás acordó la formulación del problema, la solución, el alcance y los objetivos el 2026-09-03, recogidos desde [[Producto]], fuente de la definición vigente. El borrador [[Alcance inicial de ACE]] queda como antecedente incorporado. Este acuerdo no cierra T-017 ni implica validación final del cliente o del equipo; la revisión permanece pendiente en [[R-019 - Definición de producto y objetivos para la evaluación]].

---

## Parte I

### 1. Antecedentes personales

| Nombre | RUT | Carrera | Sede |
|---|---|---|---|
| Tomás Escalante | ⟨Canal privado / Entrega final⟩ | Ingeniería en Informática | Antonio Varas |
| Matías Salas | ⟨Canal privado / Entrega final⟩ | Ingeniería en Informática | Antonio Varas |
| Paulo Loyola | ⟨Canal privado / Entrega final⟩ | Ingeniería en Informática | Antonio Varas |

### 2. Descripción del Proyecto APT

**Nombre del proyecto:** ACE — Autonomous Content Engine.

**Áreas de desempeño:** ⟨PROPUESTA validada con Malla Curricular 1446114⟩
- *Programación y Desarrollo de Software:* Construcción de componentes web, servicios y clientes de software bajo estándares de ingeniería de software.
- *Arquitectura e Integración de Plataformas:* Diseño arquitectónico distribuido, integración de sistemas heterogéneos y seguridad en la comunicación cliente-servidor.
- *Análisis y Desarrollo de Modelos de Datos:* Modelamiento relacional y persistencia local/central para soporte offline.
- *Gestión de Requerimientos y Calidad de Software:* Especificación de requisitos, diseño de interfaces, aseguramiento de la calidad y trazabilidad documental.

**Competencias:** ⟨PROPUESTA validada con Malla Curricular 1446114⟩
- Diseñar, desarrollar e integrar soluciones de software cliente-servidor y aplicaciones web/distribuidas cumpliendo estándares de calidad y seguridad.
- Modelar, consultar y administrar bases de datos relacionales y almacenamiento local para persistencia y disponibilidad de información.
- Aplicar principios de ingeniería de software, especificación formal de requerimientos y documentación técnica en el ciclo de vida del proyecto.

### 3. Fundamentación

**Relevancia del proyecto** ⟨PROPUESTA⟩

Lumina Motion es un estudio multimedia que produce experiencias visuales e interactivas. Para ACE, el foco está en pantallas instaladas en locaciones fijas.

La gestión de las pantallas de Lumina está descentralizada: utiliza herramientas y procedimientos separados, incluye cargas manuales de contenido y requiere intervención presencial. Esto dificulta el control conjunto de las pantallas y la coordinación de cambios, aumentando el tiempo operativo y el riesgo de errores.

ACE busca centralizar la administración de pantallas, contenido y programación, permitiendo su gestión a distancia y conservando la capacidad de operarlas y modificarlas localmente cuando no exista conexión a internet.

La relevancia para el campo laboral de la carrera está en que el proyecto
integra desarrollo backend, diseño de API, modelado de datos, desarrollo
frontend, comunicación en tiempo real y despliegue en infraestructura real,
sobre un requerimiento de un cliente concreto.

**Descripción del proyecto** ⟨ACORDADA CON TOMÁS — 2026-09-03⟩

ACE es una plataforma de gestión de cartelería digital para Lumina Motion que permite administrar de manera centralizada y remota las pantallas, el contenido multimedia y su programación en locaciones fijas. Contempla reproducción autónoma y cambios locales de contenido y programación sin internet, utilizando archivos disponibles en la locación; durante un corte no se puede descargar contenido del servidor remoto.

Cristóbal será el primer usuario administrador. El acceso de operadores estará funcionando desde la primera versión y limitado a sus locaciones autorizadas, aunque todavía no se utilice. La forma técnica del respaldo local continúa por definir y no se compromete una alternativa arquitectónica en esta descripción.

**Alcance de la primera versión:** administración de locaciones, sectores y pantallas; carga de medios y playlists reutilizables con orden, tiempos de exhibición y acceso limitado a locaciones autorizadas; programación por fechas y horarios para pantallas o sectores; reproducción e intervención local sin internet; y consulta básica de conectividad y última comunicación de los NUC. Quedan fuera la creación o edición audiovisual, el mantenimiento físico, una entidad cliente y funciones de suscripción o personalización SaaS, los permisos por sector y el monitoreo avanzado. Los formatos admitidos, las reglas de duración y los conflictos de programación requieren delimitación. Este alcance describe el producto a desarrollar, no software que deba entregarse completo en la primera evaluación.

**Pertinencia con el perfil de egreso:** ⟨PROPUESTA⟩

El proyecto ACE tributa directamente al perfil de egreso del Ingeniero en Informática de Duoc UC, al responder a una necesidad real de la industria (Lumina Motion) mediante la integración de desarrollo frontend y backend, arquitectura cliente-servidor distribuida, gestión de bases de datos centralizadas y locales para operación ante desconexión, y aseguramiento del ciclo de vida del software con metodologías y documentación técnica rigurosa.

**Relación con los intereses profesionales:**

- **Paulo Loyola:** Mi interés profesional se orienta al desarrollo de software con foco en frontend y en la gestión de bases de datos, complementado con una documentación técnica estructurada. En el proyecto ACE, mi labor comprende la construcción de interfaces de usuario para el control y administración del sistema, la estructuración y consumo eficiente de datos, y el mantenimiento riguroso de la documentación del software para asegurar la mantenibilidad y calidad técnica del producto.
- **Tomás Escalante:** ⟨PROPUESTA — pendiente validación Tomás⟩ Interés enfocado en el desarrollo backend y la arquitectura de software, asumiendo el diseño distribuido del sistema ACE, las APIs de integración, la lógica de sincronización y los servicios resilientes a fallas de red.
- **Matías Salas:** Mi interés profesional se orienta al desarrollo de software, la gestión del proyecto y la vinculación e interacción directa con el cliente, liderando el levantamiento continuo con Lumina Motion, la planificación operativa y la articulación funcional de las entregas.

**Factibilidad** ⟨PROPUESTA validada por equipo⟩

- *Duración:* dieciocho semanas académicas, del 10 de agosto al 12 de diciembre.
- *Equipo:* tres integrantes con roles diferenciados: Tomás Escalante (Backend/Arquitectura), Paulo Loyola (Frontend/Bases de Datos) y Matías Salas (Gestión/Player/Cliente).
- *Facilitadores:*
  1. Acceso directo al cliente a través de Cristóbal, jefe del área de informática de Lumina Motion.
  2. Existencia de documentación previa y diagramas conceptuales del proyecto.
  3. Adopción de un harness operativo asistido por IA (ACE) versionado en Git que optimiza la documentación y la velocidad de desarrollo.
- *Obstaculizadores y Mitigaciones:*
  1. *Variabilidad o fallas en el hardware físico de pantallas:* Mitigado mediante el desarrollo de un Player basado en estándares web livianos y empaquetables, compatible con múltiples plataformas.
  2. *Cortes de conectividad en locales o eventos:* Mitigado con arquitectura de almacenamiento y caché local (SQLite/IndexedDB) para reproducción en bucle autónomo sin internet.
  3. *Tiempos acotados de desarrollo:* Mitigado mediante la priorización estricta de un MVP funcional para la Semana 10 (Hito 2).
- *Materiales y recursos requeridos:*
  - Pantallas de prueba y microcomputadores/Mini PCs para despliegue de Player.
  - Servidor local en sitio para entornos sin conexión directa.
  - Infraestructura Cloud / Servidor web para API y base de datos central.
  - Entornos de desarrollo, repositorios Git y herramientas de diseño UI/UX.

---

## Parte II

### 4. Objetivos

**Objetivo general** ⟨ACORDADO CON TOMÁS — 2026-09-03⟩

Desarrollar una plataforma de gestión de cartelería digital para Lumina Motion que permita administrar de manera centralizada y remota las pantallas, el contenido y su programación en locaciones fijas, manteniendo la reproducción y permitiendo realizar cambios localmente cuando no exista conexión a internet.

**Objetivos específicos** ⟨ACORDADOS CON TOMÁS — 2026-09-03⟩

1. Implementar la administración centralizada y remota de locaciones, sectores y pantallas, con acceso diferenciado para administradores y operadores según las locaciones autorizadas.
2. Desarrollar la gestión de contenido multimedia y playlists reutilizables, permitiendo organizar su orden, configurar tiempos de exhibición y limitar el acceso al contenido autorizado.
3. Implementar la programación de playlists por fechas y horarios, con asignación a pantallas o sectores.
4. Habilitar la reproducción autónoma y la modificación local de contenido y programación sin internet, utilizando archivos disponibles en la locación.
5. Incorporar la consulta del estado básico de conectividad de los NUC, incluyendo su última comunicación con la plataforma.
6. Validar el sistema en un entorno de pruebas con el cliente, verificando gestión remota, permisos y funcionamiento con y sin conexión a internet.

### 5. Metodología

⟨PROPUESTA — marco ágil adaptado asistido por IA⟩

El equipo adopta una metodología de desarrollo iterativa e incremental basada en marcos ágiles (Scrum/Kanban) complementada con el harness colaborativo ACE (asistencia de agentes de IA para trazabilidad, documentación técnica continua y revisión de código).

**Funciones y responsabilidades:** ⟨PROPUESTA acordada con equipo⟩

- **Tomás Escalante:** Arquitectura de software, desarrollo backend, diseño de servicios y APIs de comunicación.
- **Matías Salas:** Desarrollo de software, gestión del proyecto, planificación operativa y vinculación/interacción con el cliente (Lumina Motion).
- **Paulo Loyola:** Desarrollo de software con foco en frontend, gestión y modelamiento de bases de datos, y estandarización y control de la documentación técnica.

### 6. Evidencias

⟨PROPUESTA sujeta a ratificación con docente⟩

| Tipo | Nombre | Descripción | Justificación |
|---|---|---|---|
| Avance | Informe de Definición y Planificación (Fase 1) | Documento formal de alcance, requerimientos, arquitectura y Carta Gantt. | Valida la pertinencia y factibilidad del proyecto. |
| Avance | Prototipo Funcional y API Base (Semana 10) | Demostración de panel web y comunicación básica con Player. | Demuestra avance técnico real e integración cliente-servidor. |
| Final | Plataforma ACE Desplegada (Semana 15) | Software completo operando con reproducción offline y sincronización. | Cumplimiento del 100% de los objetivos planteados. |
| Final | Manual Técnico y de Usuario | Documentación exhaustiva de instalación, uso y arquitectura. | Asegura mantenibilidad y transferencia al cliente. |

### 7. Plan de trabajo

⟨PROPUESTA elaborada en T-020 / R-016⟩

| Competencia del Perfil de Egreso | Nombre de la Actividad | Descripción | Recursos Requeridos | Duración | Responsable | Observaciones / Entregables |
|---|---|---|---|:---:|---|---|
| **C3.** Ingeniería de software y requerimientos | **1.1** Levantamiento de requerimientos | Reuniones con Lumina Motion para relevar dolores operativos. | Canal comunicación | S1 - S2 (2 sem) | Matías Salas | Requerimientos base |
| **C3.** Ingeniería de software y requerimientos | **1.2** Alcance y factibilidad | Delimitación del MVP, objetivos y análisis de viabilidad. | Docs técnicos | S2 - S3 (2 sem) | Tomás / Matías | Alcance formal |
| **C1.** Soluciones cliente-servidor distribuidas | **1.3** Selección de stack y arquitectura | Arquitectura centralizada y cliente de pantalla offline. | Herramientas diseño | S2 - S3 (2 sem) | Tomás / Paulo | Diagrama de arquitectura |
| **C3.** Ingeniería de software y requerimientos | **1.4** Elaboración Informe y Diapositivas | Redacción formal y preparación de defensa Fase 1. | Plantilla Duoc | S3 - S4 (2 sem) | Equipo | **Hito 1 (S4):** Presentación Grupal |
| **C3.** Ingeniería de software y requerimientos | **2.1** Ajustes post-feedback S4 | Incorporación de observaciones docentes al diseño. | Rúbrica | S5 (1 sem) | Equipo | Requerimientos refinados |
| **C2.** Bases de datos relacionales y locales | **2.2** Modelado de datos | Diseño del esquema relacional y almacenamiento local. | Motor DB, CASE | S5 - S6 (2 sem) | Paulo / Tomás | Diagrama ER y DDL |
| **C1.** Soluciones cliente-servidor distribuidas | **2.3** Diseño UI/UX Panel Admin | Wireframes y flujos interactivos de administración. | Figma | S5 - S6 (2 sem) | Paulo Loyola | Prototipo de interfaz |
| **C1.** Soluciones cliente-servidor distribuidas | **2.4** Especificación APIs RESTful | Definición de endpoints, payloads JSON y contratos API. | OpenAPI / Swagger | S6 (1 sem) | Tomás Escalante | Docs de API |
| **C2.** Bases de datos relacionales y locales | **3.1** Implementación Base de Datos | Despliegue de BD central y capa de acceso a datos / ORM. | Servidor DB | S7 - S8 (2 sem) | Paulo / Tomás | BD operativa |
| **C1.** Soluciones cliente-servidor distribuidas | **3.2** Desarrollo Backend Core | Endpoints de medios, pantallas y autenticación. | Framework backend | S7 - S9 (3 sem) | Tomás Escalante | API funcional |
| **C1.** Soluciones cliente-servidor distribuidas | **3.3** Desarrollo Frontend Admin | Interfaz web reactiva para pantallas y programación. | Framework frontend | S8 - S10 (3 sem) | Paulo Loyola | Panel web operativo |
| **C1.** Soluciones cliente-servidor distribuidas | **3.4** Construcción Player Base | Reproductor multimedia local para ejecución en pantalla. | Web / Electron | S8 - S10 (3 sem) | Matías / Tomás | Player base operativo |
| **C3.** Ingeniería de software y requerimientos | **3.5** Integración y validación avance | Pruebas de integración y validación con Lumina Motion. | Servidor local | S9 - S10 (2 sem) | Matías / Equipo | **Hito 2 (S10):** Entrega de Avance |
| **C3.** Ingeniería de software y requerimientos | **3.6** Revisión feedback intermedio | Ajuste de planificación según feedback del Hito 2. | Rúbrica | S11 (1 sem) | Equipo | Plan ajustado |
| **C1.** Soluciones cliente-servidor distribuidas | **4.1** Programación horaria avanzada | Lógica de calendarización por horario, fechas y sectores. | Scheduler engine | S12 - S13 (2 sem) | Paulo / Tomás | Programador integrado |
| **C1 / C2.** Persistencia y resiliencia offline | **4.2** Resiliencia offline y Player local | Caché local persistente para reproducción sin internet. | SQLite / IndexedDB | S12 - S14 (3 sem) | Tomás / Matías | Player autónomo offline |
| **C1.** Soluciones cliente-servidor distribuidas | **4.3** Sincronización y telemetría | Comunicación bidireccional y reporte de estado. | WebSockets / Polling| S13 - S14 (2 sem) | Tomás / Paulo | Telemetría en vivo |
| **C3.** Ingeniería de software y requerimientos | **4.4** Pruebas integrales de tolerancia | Simulación de cortes de red y recuperación de estado. | Banco de pruebas | S14 (1 sem) | Matías / Equipo | Informe de pruebas |
| **C1.** Soluciones cliente-servidor distribuidas | **5.1** Despliegue Staging y hardware | Instalación en servidores e integración con pantallas. | Servidor / Mini PC | S15 (1 sem) | Matías / Tomás | Sistema desplegado |
| **C3.** Ingeniería de software y requerimientos | **5.2** Consolidación Informe Final | Manuales técnico, de usuario y memoria final. | Docs oficiales | S15 (1 sem) | Paulo / Equipo | **Hito 3 (S15):** Entrega Final |
| **C3.** Ingeniería de software y requerimientos | **6.1** Validación Lumina y Defensa | Pruebas de aceptación con cliente y examen de título. | Prototipo / Demo | S16 - S18 (3 sem) | Equipo | **Hito 4 (S17-18):** Examen Final |

### 8. Carta Gantt (18 Semanas)

⟨PROPUESTA elaborada en T-020 / R-016⟩

| # | Actividad | Resp. | S1 | S2 | S3 | S4 [H1] | S5 | S6 | S7 | S8 | S9 | S10 [H2] | S11 | S12 | S13 | S14 | S15 [H3] | S16 | S17 [H4] | S18 [H4] |
|---|---|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **1.1** | Requerimientos Lumina | Matías | █ | █ | | | | | | | | | | | | | | | | |
| **1.2** | Alcance y factibilidad | Tomás/Matías | | █ | █ | | | | | | | | | | | | | | | |
| **1.3** | Stack y arquitectura | Tomás/Paulo | | █ | █ | | | | | | | | | | | | | | | |
| **1.4** | Informe y Diapositivas | Equipo | | | █ | █ | | | | | | | | | | | | | | |
| **★** | **Hito 1: Presentación Fase 1**| **Equipo** | | | | **◆** | | | | | | | | | | | | | | |
| **2.1** | Ajustes post-feedback S4 | Equipo | | | | | █ | | | | | | | | | | | | | |
| **2.2** | Modelo de datos | Paulo/Tomás | | | | | █ | █ | | | | | | | | | | | | |
| **2.3** | Diseño UI/UX Panel Admin | Paulo | | | | | █ | █ | | | | | | | | | | | | |
| **2.4** | Especificación APIs REST | Tomás | | | | | | █ | | | | | | | | | | | | |
| **3.1** | Implementación BD | Paulo/Tomás | | | | | | | █ | █ | | | | | | | | | | |
| **3.2** | Desarrollo Backend Core | Tomás | | | | | | | █ | █ | █ | | | | | | | | | |
| **3.3** | Desarrollo Frontend Admin | Paulo | | | | | | | | █ | █ | █ | | | | | | | | |
| **3.4** | Construcción Player Base | Matías/Tomás | | | | | | | | █ | █ | █ | | | | | | | | |
| **3.5** | Integración y validación | Matías/Equipo| | | | | | | | | █ | █ | | | | | | | | |
| **★** | **Hito 2: Entrega Avance** | **Equipo** | | | | | | | | | | **◆** | | | | | | | | |
| **3.6** | Feedback intermedio S10 | Equipo | | | | | | | | | | | █ | | | | | | | |
| **4.1** | Programación horaria | Paulo/Tomás | | | | | | | | | | | | █ | █ | | | | | |
| **4.2** | Resiliencia offline Player| Tomás/Matías | | | | | | | | | | | | █ | █ | █ | | | | |
| **4.3** | Sincronización y telemetría | Tomás/Paulo | | | | | | | | | | | | | █ | █ | | | | |
| **4.4** | Pruebas tolerancia fallos | Matías/Equipo| | | | | | | | | | | | | | █ | | | | |
| **5.1** | Despliegue Staging / HW | Matías/Tomás | | | | | | | | | | | | | | | █ | | | |
| **5.2** | Consolidación Informe Final| Paulo/Equipo | | | | | | | | | | | | | | | █ | | | |
| **★** | **Hito 3: Entrega Final** | **Equipo** | | | | | | | | | | | | | | | **◆** | | | |
| **6.1** | Validación Lumina y Ajustes| Matías/Equipo| | | | | | | | | | | | | | | | █ | █ | |
| **6.2** | Preparación Examen y Demo | Paulo/Matías | | | | | | | | | | | | | | | | | █ | █ |
| **★** | **Hito 4: Examen Final** | **Equipo** | | | | | | | | | | | | | | | | | | **◆** | **◆** |

---

## Resumen de lo que falta

| # | Falta | Estado / Quién responde |
|---|---|---|
| 1 | Carrera y sede de cada integrante | **Resuelto** (Ingeniería en Informática, Sede Antonio Varas). RUTs reservados para canal privado / entrega final. |
| 2 | Competencias del perfil de egreso y áreas de desempeño | **Resuelto** (incorporadas formalmente desde Malla Curricular 1446114). |
| 3 | Intereses profesionales | Paulo validado. Propuestas formuladas para Tomás y Matías, pendientes de su ratificación. |
| 4 | Metodología declarada y responsabilidades por integrante | **Resuelto** (incorporado en T-019 / Borrador). |
| 5 | Evidencias | **Resuelto** (propuesta incorporada en punto 6). |
| 6 | Recursos materiales y obstaculizadores | **Resuelto** (incorporado en factibilidad). |
| 7 | Actividades del plan de trabajo y Carta Gantt | **Resuelto** ([[T-020]] / [[R-016]]). |
| 8 | Documento de entrega montado en plantilla | Pendiente consolidación final ([[T-021]]). |

## Enlaces

- [[Auditoría Fase 1]]
- [[Arquitectura]]
- [[R-016 - Plan de trabajo y Carta Gantt]]
