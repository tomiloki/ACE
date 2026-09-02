---
tipo: borrador
estado: propuesta
fase: 1
fecha_limite: 2026-09-05
fecha: 2026-09-01
---

# Borrador Fase 1 Duoc

Sigue la estructura de `1.5_GuiaEstudiante_Fase 1_Definicion Proyecto APT.docx`.

Los campos marcados **⟨PENDIENTE⟩** requieren respuesta del equipo y no se
completaron por suposición. Los marcados **⟨PROPUESTA⟩** son redacción sugerida
que Tomás debe validar antes de usarse.

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

Lumina Motion es un estudio multimedia que produce experiencias visuales e
interactivas. Instala pantallas en centros comerciales, locales comerciales y
eventos. Hoy la operación de esas pantallas está desacoplada: parte del
contenido se carga a mano con pendrive y el resto se administra con software
propietario de pago, como MadMapper y Arena.im, sin un punto único de control.

El costo de esa fragmentación aparece cuando hay cambios de último momento:
cada pantalla o grupo de pantallas se atiende por separado, lo que consume
tiempo del equipo técnico y expone la operación a errores en vivo frente al
público del cliente.

ACE aborda ese problema con una plataforma centralizada de gestión de
pantallas, contenido y programación horaria, capaz de seguir operando cuando
la conexión a internet falla.

La relevancia para el campo laboral de la carrera está en que el proyecto
integra desarrollo backend, diseño de API, modelado de datos, desarrollo
frontend, comunicación en tiempo real y despliegue en infraestructura real,
sobre un requerimiento de un cliente concreto.

**Descripción del proyecto** ⟨PROPUESTA⟩

Desarrollar un sistema de gestión de cartelería digital que permita administrar
de forma centralizada las pantallas instaladas, el contenido multimedia y la
programación horaria, con operación de respaldo en el sitio cuando no haya
conexión a internet.

**Pertinencia con el perfil de egreso:** ⟨PROPUESTA⟩

El proyecto ACE tributa directamente al perfil de egreso del Ingeniero en Informática de Duoc UC, al responder a una necesidad real de la industria (Lumina Motion) mediante la integración de desarrollo frontend y backend, arquitectura cliente-servidor distribuida, gestión de bases de datos centralizadas y locales para operación ante desconexión, y aseguramiento del ciclo de vida del software con metodologías y documentación técnica rigurosa.

**Relación con los intereses profesionales:**

- **Paulo Loyola:** Mi interés profesional se orienta al desarrollo de software con foco en frontend y en la gestión de bases de datos, complementado con una documentación técnica estructurada. En el proyecto ACE, mi labor comprende la construcción de interfaces de usuario para el control y administración del sistema, la estructuración y consumo eficiente de datos, y el mantenimiento riguroso de la documentación del software para asegurar la mantenibilidad y calidad técnica del producto.
- **Tomás Escalante:** ⟨PROPUESTA — pendiente validación Tomás⟩ Interés enfocado en el desarrollo backend y la arquitectura de software, asumiendo el diseño distribuido del sistema ACE, las APIs de integración, la lógica de sincronización y los servicios resilientes a fallas de red.
- **Matías Salas:** ⟨PROPUESTA — pendiente validación Matías⟩ Interés orientado al desarrollo de software, la gestión del proyecto y la vinculación e interacción directa con el cliente, liderando el levantamiento continuo con Lumina Motion, la planificación operativa y la articulación funcional de las entregas.

**Factibilidad** ⟨PROPUESTA, incompleta⟩

- *Duración:* dieciocho semanas académicas, del 10 de agosto al 12 de diciembre.
- *Equipo:* tres integrantes con roles diferenciados.
- *Facilitadores:* acceso directo al cliente a través de Cristóbal, jefe del
  área de informática de Lumina Motion, y existencia de documentación previa
  del proyecto.
- *Obstaculizadores:* ⟨PENDIENTE⟩
- *Materiales requeridos:* ⟨PENDIENTE — hardware de pantallas, servidor en
  sitio, hosting⟩

---

## Parte II

### 4. Objetivos

**Objetivo general** ⟨PROPUESTA⟩

Desarrollar una plataforma centralizada de gestión de cartelería digital para
Lumina Motion, que administre pantallas, contenido y programación horaria, y
mantenga la operación ante fallas de conexión.

**Objetivos específicos** ⟨PROPUESTA⟩

1. Modelar la estructura de datos que representa sitios, sectores, pantallas,
   contenido y programación.
2. Construir una interfaz de administración que permita cargar contenido y
   definir su programación horaria.
3. Implementar la comunicación entre el servidor y las pantallas.
4. Habilitar la operación en sitio cuando no haya conexión a internet.
5. Desplegar el sistema en un entorno de pruebas y validarlo con el cliente.

> Los objetivos específicos 3, 4 y 5 dependen de decisiones técnicas todavía
> abiertas en el diagrama.

### 5. Metodología

⟨PENDIENTE — el equipo debe declarar la metodología⟩

Elementos ya existentes que pueden alimentar este punto:

- Trabajo por fases con validación del cliente.
- Reparto de responsabilidades por etapa de proyecto y foco de trabajo.
- Registro de decisiones antes de implementar.

**Funciones y responsabilidades:** ⟨PROPUESTA acordada con equipo⟩

- **Tomás Escalante:** Arquitectura de software, desarrollo backend, diseño de servicios y APIs de comunicación.
- **Matías Salas:** Desarrollo de software, gestión del proyecto, planificación operativa y vinculación/interacción con el cliente (Lumina Motion).
- **Paulo Loyola:** Desarrollo de software con foco en frontend, gestión y modelamiento de bases de datos, y estandarización y control de la documentación técnica.

### 6. Evidencias

⟨PENDIENTE — la guía exige acordarlas con el docente⟩

| Tipo | Nombre | Descripción | Justificación |
|---|---|---|---|
| ⟨PENDIENTE⟩ | | | |

### 7. Plan de trabajo

⟨PENDIENTE — requiere las competencias del perfil de egreso, que encabezan
cada fila de la tabla exigida⟩

Columnas requeridas: competencia, nombre de la actividad, descripción,
recursos, duración, responsable y observaciones.

> Vale 10 puntos. Es el indicador 7.

### 8. Carta Gantt

⟨PROPUESTA — calendario académico real, actividades por validar⟩

| Semana | Fechas | Hito de la asignatura |
|---|---|---|
| S1 | 10 – 15 ago | Definición del proyecto |
| S2 | 17 – 22 ago | Cronograma y tecnologías |
| S3 | 24 – 29 ago | Cronograma y tecnologías |
| **S4** | **31 ago – 5 sep** | **Presentación grupal — evaluada** |
| S5 | 7 – 12 sep | Retroalimentación e inicio de desarrollo |
| S6 | 14 – 19 sep | Actualización de objetivos y cronograma |
| S7 | 21 – 26 sep | Desarrollo |
| S8 | 28 sep – 3 oct | Desarrollo |
| S9 | 5 – 10 oct | Desarrollo |
| **S10** | **12 – 17 oct** | **Entrega de avance — evaluada** |
| S11 | 19 – 24 oct | Retroalimentación |
| S12 | 26 – 31 oct | Desarrollo |
| S13 | 2 – 7 nov | Desarrollo |
| S14 | 9 – 14 nov | Desarrollo |
| **S15** | **16 – 21 nov** | **Entrega final del proyecto — evaluada** |
| S16 | 23 – 28 nov | Retroalimentación |
| **S17** | **30 nov – 5 dic** | **Presentación final — evaluada** |
| **S18** | **7 – 12 dic** | **Presentación final — evaluada** |

Las actividades del proyecto se superponen a esta grilla una vez definido el
plan de trabajo del punto 7.

---

## Resumen de lo que falta

| # | Falta | Estado / Quién responde |
|---|---|---|
| 1 | Carrera y sede de cada integrante | **Resuelto** (Ingeniería en Informática, Sede Antonio Varas). RUTs reservados para canal privado / entrega final. |
| 2 | Competencias del perfil de egreso y áreas de desempeño | **Resuelto** (incorporadas como propuesta formal desde Malla Curricular 1446114). |
| 3 | Intereses profesionales | Paulo validado. Propuestas formuladas para Tomás y Matías, pendientes de su ratificación. |
| 4 | Metodología declarada y responsabilidades por integrante | Responsabilidades incorporadas como propuesta. Metodología de trabajo en desarrollo por Tomás ([[T-019]]). |
| 5 | Evidencias | Equipo con el docente ([[T-019]]) |
| 6 | Recursos materiales y obstaculizadores | Equipo ([[T-019]] / [[T-020]]) |
| 7 | Actividades del plan de trabajo | Equipo ([[T-020]]) |
| 8 | Documento `1.5_APT122_SumativaFase1.docx` | Equipo |

## Enlaces

- [[Auditoría Fase 1]]
- [[Arquitectura]]
