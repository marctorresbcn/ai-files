# Handoff — {{titulo_tarea}}

<!-- Título: una línea que identifique la tarea sin ambigüedad.
     Ej: "Refactor módulo auth", "Prototipo integración SDK Stripe", "Fix bug paginación" -->

**Sesión origen:** {{sesion_origen}}  
**Propósito:** {{proposito_una_frase}}  
**Patrón:** {{patron}}

<!-- Patrón: elige uno:
     - Delegación pura — la sesión origen no necesita resultados de vuelta
     - Ida y vuelta — la nueva sesión debe generar un handoff de vuelta con lo aprendido -->

---

## Contexto

<!-- Solo lo que el agente receptor necesita para entender la situación.
     No copies lo que ya está en otros archivos — usa punteros (ver sección "Archivos relevantes").
     Responde: ¿de dónde viene esta tarea? ¿qué decisiones o trabajo previo son relevantes?
     3-6 líneas suele ser suficiente. Si necesitas más, es señal de que el scope no está claro. -->

**Último estado conocido:** {{ultimo_estado}}

<!-- Dónde se quedó exactamente la sesión anterior. Qué se intentó, qué falló, dónde está el bloqueo.
     Ej: "Se intentó levantar el contenedor pero falló el handshake con la BD (ver log en logs/docker.out)"
     Ej: "El endpoint /refresh devuelve 401 intermitente. Se sospecha condición de carrera en el refresh handler."
     Esto evita que el nuevo agente tropiece con la misma piedra antes de entender dónde estaba el problema. -->

---

## Tarea

<!-- Qué hay que hacer exactamente. Sé específico: el agente no tiene tu contexto mental.

     Incluye:
     - Qué se espera como resultado (funcionalidad, archivo, PR, análisis...)
     - Restricciones técnicas relevantes (versiones, convenciones, dependencias)
     - Casos edge o condiciones que el agente debe tener en cuenta

     Incluye también lo que NO entra en scope. Esto es tan importante como lo que sí entra:
     evita que el agente se meta en trabajo que corresponde a otra sesión o tarea. -->

---

## Archivos relevantes

<!-- Lista de archivos, documentos o recursos que el agente debe leer.
     No copies su contenido aquí — usa la ruta o el enlace y deja que el agente los lea.

     Ej:
     - `src/auth/index.ts` — módulo principal a refactorizar
     - `docs/arquitectura.md` — contexto de la arquitectura actual
     - github.com/org/repo/issues/42 — issue relacionado

     Si hay recursos que NO debe tocar, indícalo explícitamente. -->

---

## Decisiones ya tomadas

<!-- Qué está decidido y no se debe cuestionar en esta sesión.
     Ahorra al agente tiempo y evita que reabra debates ya cerrados.

     Ej:
     - Stack: Node.js + TypeScript (sin cambios)
     - Puerto del nuevo servicio: 3001
     - Base de datos compartida por ahora, sin cambios de schema

     Si no hay nada decidido todavía, elimina esta sección. -->

---

## Skills sugeridas

<!-- Skills que el agente debería invocar al inicio de la sesión.
     Esto orienta el tono y las convenciones de trabajo desde el principio.

     Ej:
     - `skill: diagnostics` — para analizar dependencias antes de tocar código
     - `skill: typescript` — convenciones del proyecto
     - `skill: bbq` — si la nueva sesión va a ser de planificación

     Elimina esta sección si no aplica ninguna. -->

---

## Output esperado

<!-- Qué debe producir esta sesión cuando termine. Sé concreto.
     Incluye siempre un criterio de validación: cómo demuestra el agente que ha terminado con éxito.

     Ej:
     - Rama `feat/auth-service` con el servicio extraído
     - PR abierto contra `main`
     - Validación: `npm run test:auth` en verde y linter sin errores

     Para patrón ida y vuelta, especifica que se espera un nuevo handoff.md con:
     - Lo que funcionó y lo que no
     - Decisiones tomadas durante el prototipo
     - Lo que no quedó capturado en el código pero es relevante para la sesión padre -->

---

*Generado desde {{sesion_origen}} — guardado en /tmp, desechable*
