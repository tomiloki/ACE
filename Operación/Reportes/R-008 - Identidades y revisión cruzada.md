---
tipo: reporte
estado: cerrado
revision_humana: aprobada
modulo: "[[Operación y reportaje de ACE]]"
tarea: "[[T-002 - Diseñar comunicación entre agentes y equipo]]"
fecha: 2026-09-01
---

# Identidades y revisión cruzada

## Reporte del ejecutor

### Resumen

ACE incorporó identidades de trabajo independientes del modelo y probó una revisión cruzada donde el revisor informa y el ejecutor corrige. El piloto mejoró la trazabilidad, pero reveló que la evidencia no debe dispersarse.

La convención evolucionó: un agente puede revisar su propio trabajo con recomendación `ejecutor`; con `agente_externo`, el revisor debe ser distinto. La revisión completa vive en el reporte de la tarea principal y la tarea conserva su estado resumido.

### Implicancias

- La identidad permite seguir responsabilidades aunque cambie el modelo.
- Los agentes declaran etapa y foco; el territorio corresponde a subagentes.
- La revisión recomienda quién revisa: `ejecutor`, `agente_externo`, `humano` o `equipo`.
- Heimdall es una opción externa, no una parada obligatoria ni un agente autónomo.
- El usuario decide cuándo y quién revisa; la recomendación no activa nada.

### Detalle técnico y evidencia

- Implementación inicial: `54d4058 feat: add agent identities and cross-review workflow`.
- [[T-011 - Probar revisión cruzada entre agentes]] conserva ambos veredictos y las correcciones.
- El piloto separó identidad y modelo, impidió correcciones silenciosas del revisor y preservó ejecutor y revisor.
- La convención vigente está en [[Sistema de reportaje ACE]].

### Abierto

- [[T-013 - Definir harness compartido mínimo de ACE]] debe cargar efectivamente estas reglas.
- [[T-014 - Probar el harness compartido en una tarea real]] debe comprobar el flujo completo.
- La revisión automatizada se definirá más adelante; aquí no se lanza Heimdall.

## Revisión

Tomás revisó y aprobó el reporte junto con los otros reportes estructurales abiertos. Antes del cierre se corrigieron las referencias a tareas para que coincidan con sus nombres reales.

## Enlaces

- [[Registro de agentes ACE]]
- [[Registro de subagentes ACE]]
- [[Heimdall - Revisión independiente]]
- [[Sistema de reportaje ACE]]
- [[T-002 - Diseñar comunicación entre agentes y equipo]]
- [[T-011 - Probar revisión cruzada entre agentes]]
- [[T-013 - Definir harness compartido mínimo de ACE]]
- [[T-014 - Probar el harness compartido en una tarea real]]
