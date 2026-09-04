---
tipo: documentacion
estado: propuesta
modulo: "[[Producto y documentación para la primera evaluación]]"
creado: 2026-09-04
---

# Prototipos Visuales y Wireframes UI/UX — Plataforma ACE

Especificación y descripción de las versiones exploradas para la interfaz de usuario del sistema de gestión de cartelería digital ACE para Lumina Motion.

---

## 1. Versión 1: "ACE Command Center" (Enfoque Operacional y Red de Pantallas)

Diseñada para la supervisión y monitoreo en tiempo real de múltiples locaciones comerciales (Mall Costanera Center, Plaza Norte, Alto Las Condes).

### Componentes:
- **Banner de Resiliencia de Red:** Indicador en tiempo real de pantallas online vs. pantallas operando de forma autónoma con almacenamiento local (caché SSD).
- **Selector de Locaciones y Filtros:** Permite aislar sitios y sectores específicos.
- **Matriz de Tarjetas de Pantallas:**
  - Miniatura con reproducción de video en vivo.
  - Indicador de resolución (`1080x1920` vertical / `2160x3840` 4K).
  - Telemetría térmica y de hardware del NUC (`42°C`, uso de CPU).
  - Estado de caché (`100% Cached`).
  - Nombre de la lista de reproducción (Playlist) actualmente activa.
- **Barra de Navegación Lateral:** Accesos directos a Dashboard, Pantallas, Bóveda de Medios, Programador y Analítica.

---

## 2. Versión 2: "ACE Playlist Studio" (Enfoque Composición, Scheduler y Simulador 9:16)

Diseñada para la creación, curaduría de contenidos multimedia, calendarización horaria y simulación de pantalla vertical.

### Componentes:
- **Bóveda de Medios (Media Asset Vault):**
  - Grilla de tarjetas arrastrables con videos, imágenes y animaciones.
  - Indicador visual de duración (`00:15s`, `00:30s`, `01:00m`) y formato.
- **Línea de Tiempo Multi-Pista (Timeline Scheduler):**
  - Regla horaria de 24 horas (08:00 a 22:00) con bloques programados por colores (`Morning Brand Loop`, `Flash Promo`, `Evening Showcase`).
  - Pistas secundarias para eventos especiales y spots de sobreescritura.
- **Simulador de Tótem en Vivo (9:16 Preview):**
  - Ventana interactiva que renderiza el encuadre exacto del tótem vertical.
  - Controles de reproducción (Play/Pause, scrub, contador de frames).
  - Medidor de capacidad de almacenamiento local del NUC (`78.4GB / 128GB SSD`).
  - Badge de verificación: `Autonomous Offline Mode: Ready`.
- **Botón de Publicación:** Acción `Publish to NUC Players` para desplegar la nueva programación a los dispositivos en terreno.

---

---
## 3. Vistas de Media Library (Bóveda y Gestión de Medios)

### 3.1 Versión 1: "Visual Asset Vault & Quick Inspector"
Diseñada para la gestión visual ágil, carga rápida de archivos e inspección detallada de metadatos.
- **Zona de Carga Inteligente (Drag-and-Drop):** Área superior con detección automática de tipo de medio y optimización para el almacenamiento local de los NUCs.
- **Diferenciación de Duración:** Distingue duración nativa en videos (`00:20s (Native)`) de la duración asignada en imágenes/banners (`00:10s (Configured)`).
- **Filtros por Campaña y Tags:** Píldoras interactivas (`Costanera Retail`, `Mall Plaza Ads`, `Holiday 2026`, `Emergency Banners`).
- **Inspector Lateral (Quick Asset Inspector):** Panel derecho con reproductor previo, edición de tags y botón modal `Assign to Screens`.
- **Estado de Resiliencia:** Badge verde `100% NUC Cached` que confirma que el medio ya fue descargado localmente por los NUCs de pantalla.

### 3.2 Versión 2: "Folder & Campaign Manager with Screen Target Matrix"
Diseñada para la organización por clientes, carpetas jerárquicas y distribución directa sobre planos de pantallas.
- **Árbol de Carpetas (Folder Tree):** Navegación estructurada (`Lumina Motion Clients > Costanera Center > Retail Promos > Autumn 2026`).
- **Indicador de Salud de Sincronización:** Badge consolidado `Sync Health: Downloaded to 14/14 Local NUCs`.
- **Selector Interactivo de Pantallas (Screen Target Selector):** Plano visual de tótems y pantallas LED del mall con acción directa `1-click Deploy Asset to Loop`.

---

## Comparativa de Usabilidad — Vistas de Media Library

| Dimensión | Versión 1: Visual Asset Vault | Versión 2: Folder & Campaign Hub |
|---|---|---|
| **Estructura Principal** | Cuadrícula visual con zona de carga superior e inspector lateral. | Árbol jerárquico de carpetas con cuadrícula y plano de distribución de pantallas. |
| **Gestión de Duración** | Distingue duración nativa (video) vs. duración configurada (imagen/animación). | Duración resumida en tarjeta con metadata expandible. |
| **Acción Principal** | Inspección rápida y asignación modal a pantallas. | Despliegue en 1 clic hacia el loop activo de las pantallas seleccionadas. |
| **Control Offline** | Badge individual `100% NUC Cached` por archivo. | Badge consolidado de red `Downloaded to 14/14 Local NUCs`. |
