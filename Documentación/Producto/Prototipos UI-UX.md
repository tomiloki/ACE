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

## Comparativa de Usabilidad

| Dimensión | Versión 1 (Command Center) | Versión 2 (Playlist Studio) |
|---|---|---|
| **Objetivo Central** | Diagnóstico rápido, telemetría y salud de pantallas. | Programación horaria y curaduría multimedia. |
| **Control Offline** | Muestra qué pantallas están en corte de red. | Asegura que el contenido esté 100% precargado antes de emitir. |
| **Simulación Visual** | Miniaturas en grilla. | Reproductor a escala vertical 9:16. |
| **Rol de Usuario** | Operador técnico / Soporte. | Gestor de contenidos / Diseñador multimedia. |
