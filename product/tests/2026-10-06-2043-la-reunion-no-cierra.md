---
opportunity: la-reunion-no-cierra
solutions: product/solutions/2026-10-06-2035-la-reunion-no-cierra.md
status: designed
date: 2026-10-06
---

# Solution tests for: La reunión no cierra

## Why test

En testeo paralelo **A1 `cierre-confirmado`** y **A2 `recap-de-decisiones`** (status `testing-several` en el archivo de soluciones). Las dos tienen el dolor evidenciado (`real`: 9/10 reescriben a mano 20–60 min, 6 ejecuciones erradas con costo; `survey`: 24% de decisiones sin registro, tema #1 de la abierta) y ninguna tiene evidencia de solución: nadie reaccionó todavía a una lista decisión · dueño · fecha · motivo (A1), y la única reacción real a un recap es **en contra** de la versión actual —6/10 lo corrigen o abandonan, una decisión inventada se ejecutó— (A2). Lo que falta probar es distinto en cada una: en A1, la **conducta** (que el líder confirme en el momento y deje de reescribir); en A2, la **precisión** (que la máquina distinga decisión de comentario sin inventar). Por eso una se testea con personas y la otra con transcripciones y una clave de respuestas.

La `[viability]` #1 del registro (IT nombra el registro auditable frente a Compras) no se testea aquí: ya tiene instrumento en la agenda de la oportunidad (`/design-interview` a responsables de Collaboration Services, para el 24 de noviembre). Si IT no lo nombra, el archivo de soluciones ya fija `back-to-research` para las dos alternativas.

**Dependencia entre tests:** T2 usa como set de entrada las reuniones de T1 que se graben con consentimiento, y como clave de respuestas la lista que el líder confirmó en T1. T1 corre primero; T2 arranca cuando T1 cierra el campo.

## T1. cierre-confirmado: el cierre acompañado

- **Test status:** ready
- **Belief under test:** `[feature: cierre-confirmado] [value]` "Si al final de una reunión que decide se le ofrece al líder una lista corta decisión · dueño · fecha · motivo, la confirma en el momento en la mayoría de los casos y el equipo ejecuta lo confirmado; deja de reescribir después." (#11 del registro)
- **Risk:** [value]
- **Test type:** concierge
- **What we do:**
  1. Reclutar 5 Team Leads del pool de la encuesta (criterio abajo). Se les pide inscribir sus reuniones recurrentes de 5+ participantes de las próximas 2 semanas en las que se tomen decisiones (meta: 3 por líder, ~15 en total). Se les dice que "vamos a probar una forma de cerrar la reunión"; no se les muestra ninguna pantalla ni se describe A1 como producto.
  2. Una persona del equipo (el concierge, sin cámara, presentado como observador) asiste a cada reunión y va anotando decisiones candidatas: qué, quién, para cuándo, por qué, y qué se derivó a otra reunión.
  3. Cinco minutos antes del final previsto, el concierge pega la lista en el chat de esa reunión (o en las notas nativas, si el líder las usa) con la plantilla de Material, y dice una sola frase: "Esto es lo que anoté como decidido; ¿lo confirmás?". No argumenta ni completa huecos: si el líder no sabe el dueño, el hueco queda en blanco y se registra.
  4. El líder confirma tal cual, corrige y confirma, la pospone ("lo cierro después") o la ignora. El concierge registra cuál de las cuatro, cuánto duró el cierre y si el líder la leyó en voz alta al equipo.
  5. Al día siguiente (≤24 h), el concierge le pide al líder lo que haya producido después de la reunión sobre esas decisiones —ticket, correo, recap corregido, mensaje en el canal— y registra si existe y si su contenido difiere de la lista confirmada.
  6. A los 7 días, una pregunta por chat: "De lo que confirmaste, ¿algo se ejecutó distinto o se reabrió?" Se registra la respuesta literal.
- **With whom:** 5 Team Leads del segmento (cuenta >1.000 licencias, reuniones recurrentes de 5+ en las que se decide), reclutados del pool de 64 candidatos de la encuesta (product/insights/2026-09-29-2037-colaboracion-en-vivo-fuera-de-teams.md, §11). Orden de reclutamiento: primero quienes ya describieron la reescritura en entrevista y tienen 4+ reuniones por semana (Tomás R-113, Javier R-097, Martina R-224), después nuevos del pool con "4 o más" reuniones (R-085, R-132, R-159, R-229, R-234, R-238) para no probar solo con quienes ya nombraron el problema. Mezcla buscada: al menos uno de variante datos (perfil Gustavo: Diego R-036) y al menos uno que no sale de Teams (R-143, R-153). Incentivo: ninguno más allá de recibir la lista confirmada de sus reuniones.
- **Material needed:** (a) una plantilla de una página con cinco columnas —decisión · dueño · fecha · motivo · derivado a otra reunión— en texto plano pegable en el chat de Teams; sin votación, sin transcripción, sin integración con Jira o Notion, sin ninguna marca de producto: tiene que parecer una nota, no una función. (b) Un guion de tres líneas para el concierge: cómo se presenta al inicio, la frase única del cierre, la pregunta del día siguiente y la de los 7 días, en ese orden y sin variantes. (c) La hoja de captura por reunión: líder, fecha, tipo de reunión, participantes, herramienta de trabajo usada, nº de decisiones listadas, huecos en blanco (dueño/fecha/motivo), resultado del cierre (confirmó tal cual / corrigió y confirmó / pospuso / ignoró), minutos del cierre, leída en voz alta (sí/no), reescritura al día siguiente (no / sí, misma lista copiada / sí, contenido distinto — con el artefacto adjunto), respuesta literal a los 7 días. Nada más: sin encuesta de satisfacción, sin preguntas de "¿te gustó?".
- **Material:** product/tests/materials/t1-cierre-confirmado/ — `plantilla-cierre.md` (a), `guion-concierge.md` (b, con el paso a paso por reunión), `hoja-de-captura.md` (c, con el resumen del campo y la lectura de S1–S3), `mensaje-de-reclutamiento.md` (orden de envío del With whom). La hoja y el mensaje llevan además el consentimiento de grabación que pide la dependencia T1 → T2.
- **Duration:** 2 semanas de campo + 1 semana de seguimiento (los 7 días de la última reunión). Inicio 13 de octubre, cierre del campo 24 de octubre, cierre de seguimiento 31 de octubre. Entra antes de la compuerta de fines de noviembre.
- **Signal and threshold:** Sobre las reuniones en las que se tomó al menos una decisión (se excluyen las que no decidieron; si quedan menos de 10, el test es `inconclusive`):
  - **S1, confirmación en el momento:** proporción de reuniones en las que el líder confirmó la lista (tal cual o corregida) antes de que terminara la llamada. **Umbral: ≥ 2/3** (con 15 reuniones, ≥ 10). "Pospuso" e "ignoró" cuentan como no confirmada.
  - **S2, fin de la reescritura:** entre las reuniones confirmadas, proporción en las que al día siguiente el líder **no** produjo un registro aparte con contenido distinto de la lista (copiar la misma lista a Jira o al canal no es reescritura; un recap corregido o un correo con otra versión sí lo es). **Umbral: ≥ 2/3.**
  - **S3, ejecución (secundaria, no decide):** respuestas a los 7 días en las que algo confirmado se ejecutó distinto o se reabrió. Se reporta; con 15 reuniones y una semana no alcanza para medirla.
  - Se registra además la duración del cierre: alimenta la creencia `[usability]` de A1 (<5 min), que no se decide aquí.
- **Decision rule:** `continue` si S1 ≥ 2/3 y S2 ≥ 2/3 · `change` si S1 ≥ 2/3 pero S2 < 2/3 (confirma pero igual reescribe: el valor está en entregar donde vive el trabajo, no en capturar; A3 `decision-al-ticket` sale de parked y compite) · `change` si S1 < 2/3 pero la mayoría de las no confirmadas son "pospuso" y el líder confirmó dentro de las 24 h (el cierre no es en vivo sino asíncrono: otra versión, otro test) · `discard` si S1 < 1/2 sin patrón de posposición (el líder no quiere un cierre estructurado aunque se lo den hecho; A5 cae con A1).
- **Expected provenance:** real (Team Leads del pool). Si la primera corrida se hace con compañeros de cursada o roles actuados, es `synthetic`: sirve para ensayar el guion y la hoja de captura, no mueve la creencia #11.
- **Next step if it passes:** Wizard of Oz dentro de Teams: un componente Loop "Decisiones de hoy" que aparece solo al final de la reunión (operado a mano por detrás), con 15–20 líderes durante 4 semanas y sin acompañante en la llamada, mismas señales S1 y S2 con umbral ≥ 2/3; en paralelo, `usability-test` del prototipo con 5 líderes para la creencia `[usability]` (confirmar en < 5 min). Si pasan, `ready for spec`.

## T2. recap-de-decisiones: precisión contra una clave

- **Test status:** designed
- **Belief under test:** `[feature: recap-de-decisiones] [feasibility]` "Una lista decisión · dueño · fecha · motivo generada a partir de la transcripción y de lo ocurrido en el artefacto compartido distingue decisión de comentario, asigna dueño y motivo, y no inventa decisiones, con precisión suficiente para que el líder la confirme sin reescribirla." (#12 del registro)
- **Risk:** [feasibility]
- **Test type:** technical-test
- **What we do:**
  1. **Set de entrada:** las reuniones de T1 grabadas con consentimiento de todos los participantes (meta 10, mínimo 8). Por reunión: transcripción (la de Teams), el chat de la reunión, y un **registro del artefacto** en texto: lo que el concierge anotó que pasó fuera del audio (votación en el tablero y resultado, filtro aplicado en el dashboard, hilo donde quedó la razón) o, si existe, el export del artefacto. Las grabaciones no salen del tenant del participante o se anonimizan antes de usarse; esto anticipa la restricción de compliance de la oportunidad.
  2. **Clave de respuestas:** por reunión, la lista que el líder confirmó en T1 (lo confirmado es la verdad) más, marcadas por el concierge, las "trampas": ideas o propuestas que se dijeron y **no** fueron decisión (el "podríamos pasar el release al 20" de Paula).
  3. **Generación:** un prompt v1 con formato de salida fijo (decisión · dueño · fecha · motivo · fuente: audio/artefacto/chat) corre sobre cada reunión. Se corre también el **baseline**: el recap genérico actual (Copilot) sobre la misma transcripción, y se lo califica con la misma clave.
  4. **Calificación a ciegas:** dos personas, sin saber qué salida es de qué prompt, califican ítem por ítem: decisión correcta (está en la clave) / decisión inventada (no está en la clave y no aparece en la transcripción como decisión, o es una trampa) / decisión omitida (está en la clave y no en la salida) / dueño correcto / motivo presente y coincide con la clave. Desacuerdos se resuelven en conjunto y quedan anotados.
- **With whom:** sin participantes: dueño tech (un ingeniero arma el prompt y corre el set; el PM arma la clave con el concierge). Las personas del segmento ya aportaron lo suyo en T1.
- **Material needed:** (a) el prompt v1, con el formato de salida fijo y la instrucción explícita de no listar nada que no haya sido decidido; (b) el set de entrada por reunión (transcripción + chat + registro del artefacto, anonimizados), (c) la clave de respuestas por reunión con las trampas marcadas, (d) la rúbrica de calificación con los cinco códigos de arriba y ejemplos de borde (¿"quedamos en revisarlo el jueves" es decisión o derivación?), (e) la hoja de captura por ítem y por reunión, con las mismas columnas para la salida de A2 y para el baseline. Deliberadamente fuera: ninguna interfaz, ninguna integración, ninguna confirmación del líder sobre la salida generada — eso es el siguiente paso.
- **Material:** (lo agrega /build-solution-test)
- **Duration:** 1 semana después del cierre del campo de T1: del 27 de octubre al 7 de noviembre (armar clave y prompt la primera semana en paralelo con el campo; correr y calificar la segunda).
- **Signal and threshold:** Agregado sobre el set (mínimo 8 reuniones; con menos, `inconclusive`):
  - **S1, precisión:** de los ítems generados, proporción que son decisiones de la clave. **Umbral: ≥ 80%.**
  - **S2, cobertura:** de las decisiones de la clave, proporción que aparece en la salida. **Umbral: ≥ 70%.**
  - **S3, decisiones inventadas:** reuniones con al menos una decisión inventada. **Umbral: ≤ 2 de 10** (≤ 1 de 8), y nunca más de una por reunión.
  - **S4, dueño correcto:** entre las decisiones acertadas, proporción con el dueño de la clave. **Umbral: ≥ 70%.**
  - **Contra el baseline:** A2 tiene que superar al recap genérico en S1 y S3; si no lo supera, no hay versión nueva que probar aunque pase los umbrales.
  - El motivo se reporta (presente/coincide) y no decide: es la parte que más depende del registro del artefacto, que en este set lo escribe un humano.
- **Decision rule:** `continue` si S1–S4 pasan y supera al baseline · `change` si S1 y S3 pasan pero S2 < 70% (la máquina es confiable en lo que dice pero omite: versión "lista para completar", la máquina propone y el líder agrega; necesita su propio test) · `change` si lo que falla es solo S4 o el motivo y la falla se concentra en las reuniones sin registro del artefacto (la entrada del artefacto es lo crítico: la `[feasibility]` del artefacto bajo compliance pasa a ser el siguiente test, con tech) · `discard` si S3 falla (inventa en 3+ reuniones) o S1 < 60%: no supera al recap actual y repite el abandono de 6/10.
- **Expected provenance:** real (reuniones reales del segmento grabadas en T1). Si T1 no reúne 8 reuniones grabables y se usan reuniones de la cursada o simuladas, `synthetic`: sirve para afinar el prompt y la rúbrica, no mueve la creencia #12.
- **Next step if it passes:** Wizard of Oz para la creencia `[value]` de A2 (a registrar entonces): el líder recibe la lista generada al terminar la reunión, con un operador por detrás que corre el prompt y la publica sin tocarla, en 10 reuniones; señal = la confirma con ≤ 1 línea editada en ≥ 2/3 de las reuniones y no corrige 10 min después (baseline de Paula). Si pasa, `ready for spec`.

## Results
(lo agrega /analyze-solution-tests)

## Decision
(lo agrega /analyze-solution-tests)
