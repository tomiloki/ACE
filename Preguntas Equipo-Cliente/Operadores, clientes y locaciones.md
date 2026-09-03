# Operadores, clientes y locaciones

**Pendiente de conversar con Cristóbal y el equipo.**

## Contexto y pregunta

Según el entendimiento actual, habría un operador por locación y posiblemente un cliente por locación. Falta confirmar esa realidad con Cristóbal; estas relaciones podrían cambiar en el futuro y no deben tratarse todavía como restricciones del modelo.

**¿Qué relaciones entre operadores, clientes y locaciones debe soportar ACE desde el inicio, y cuáles pueden quedar para después? ¿Necesitamos modelar al cliente o basta inicialmente con locaciones y accesos asignados?**

## Casos a confirmar

- Un operador gestiona varias locaciones, o varios operadores comparten una locación.
- Un cliente tiene varias locaciones, o una locación atiende a varios clientes.
- Qué contenido y playlists pueden compartirse y quién puede verlos, modificarlos y utilizarlos.
- Cuáles de estos casos existen hoy, cuáles son próximos y cuáles son solo posibilidades.

## Alternativas e implicancias

**A. Locaciones y permisos, sin entidad cliente inicialmente**
- Menos estructura inicial; usuarios y contenido se vinculan a las locaciones autorizadas.
- No representa por separado la pertenencia del contenido a un cliente; incorporarla después podría exigir migración.

**B. Cliente explícito, además de locaciones y permisos**
- Permite representar pertenencia y agrupación por cliente.
- Agrega relaciones y reglas que deben justificarse con casos reales; no implica construir suscripciones ni un SaaS completo.

En ambas alternativas, pertenecer al mismo cliente no concede acceso automático a todas sus locaciones o contenidos. El administrador global puede acceder al conjunto; los operadores, únicamente a lo autorizado. **Ninguna alternativa está elegida.**
