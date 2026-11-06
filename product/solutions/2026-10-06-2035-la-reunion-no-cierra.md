---
opportunity: la-reunion-no-cierra
status: testing-several
chosen: cierre-confirmado, recap-de-decisiones
tests: product/tests/2026-10-06-2043-la-reunion-no-cierra.md
date: 2026-10-06
---

# Solutions for: La reunión no cierra

Exploración sobre `product/opportunities/2026-10-06-2016-la-reunion-no-cierra.md`. Hecha antes de la compuerta que la agenda fijaba para fines de noviembre: las celdas de viabilidad y feasibility reflejan esa falta de evidencia, no se inventaron.

## Lo que dice hoy la evidencia

- `[value]` (#2 del registro) — **confirmada en calidad, abierta en extensión**: 9/10 Team Leads reescriben a mano lo decidido (20–60 min, siempre el líder) y 6 cuentan ejecuciones erradas con costo concreto (`real`, product/insights/2026-09-29-2100-entrevistas-team-leads-colaboracion-en-vivo.md, insight 1). 24% de las decisiones sin registro, 23% en Slack/WhatsApp, "registro y continuidad" tema #1 de la abierta (`survey`, product/insights/2026-09-29-2037-colaboracion-en-vivo-fuera-de-teams.md, Q9/Q11). Falta el n del segmento.
- Por qué no alcanza lo que existe (`real`): el recap de IA nivela decisión y comentario, no asigna dueño, no ve el artefacto, a veces inventa decisiones (6/10 lo corrigen o abandonan — insight 2); notas y Whiteboard se pierden al recrear la serie o reprogramar (insight 3); 31% no sabe que existen las notas (`survey`, Q10).
- `[viability]` (#1 del registro) — **sin evidencia**: ninguna entrevista fue a IT. Señales: compliance aparece 5 veces sin preguntarlo (`survey`) y en Lucía F. (`real`); el mercado regala la colaboración en vivo y cobra control de IT e IA en el escalón superior; nadie vende "decisiones con dueño" (`secondary`, product/research/2026-09-16-1313-colaboracion-en-vivo-dentro-de-la-videollamada.md).

## Baseline: lo que hace hoy el Team Lead

Reescribe a mano lo decidido después de la reunión: un ticket por acuerdo en Jira (Tomás, 20 min), el recap de Copilot corregido (Paula, 10 min) o reescrito entero (Javier, 30 min), un correo con "qué filtro y qué gráfico" (Diego), una captura de pantalla pegada en Confluence (Lucía F., Sofía) — y cuando se demora o queda ambiguo, el equipo ejecuta otra cosa (`real`, insights 1–3). En la encuesta: 24% no registra, 23% queda en Slack/WhatsApp, ~20 usan el recap "con un pero" (`survey`, Q9). Cualquier alternativa tiene que ahorrar esos 20–60 min **y** evitar la ejecución errada; una sola de las dos no justifica el cambio.

## Alternativas

### A1. Cierre confirmado (`cierre-confirmado`) — la más chica que podría funcionar
Al terminar la reunión (o cuando el líder lo pide), Teams le muestra una lista corta para llenar o confirmar: decisión · dueño · fecha · motivo, más "derivado a otra reunión". Se publica a todos los asistentes, hablaran o no, y queda atada a la serie o al equipo, no al chat de esa ocurrencia. Mecanismo: captura humana en el momento. Ataca la reescritura posterior y la ambigüedad. Para Valeria Ortiz (primary) y Gustavo Ferreyra (secondary) si el motivo admite "con este filtro". Reemplaza el ticket a mano y el correo de cierre. Absorbe "cierre estructurado" y "registro de qué se derivó".

### A2. Recap de decisiones que lee el artefacto (`recap-de-decisiones`)
Copilot produce esa misma lista estructurada, sola: toma como entrada el audio y lo que pasó en el artefacto (votación en el tablero, filtro del dashboard, hilo donde quedó la razón) y pide confirmación explícita del líder antes de publicar. Mecanismo: automatizar la captura. Ataca los 10–30 min de corregir el recap y el "convierte ideas en decisiones". Para Valeria y Gustavo; Javier, Martina y Paula son su caso de prueba. Reemplaza el recap de dos páginas. Absorbe "recap que lea el artefacto".

### A3. La decisión nace donde vive el trabajo (`decision-al-ticket`)
Cada decisión confirmada se crea directamente como ticket en Jira, entrada en Confluence, ADR o comentario en el dashboard, con enlace al minuto de la reunión y a la vista del artefacto. Mecanismo: eliminar la reescritura entregando al destino. Ataca "el qué queda en Jira, el por qué se pierde". Para Gustavo y la mitad del corpus que no sale de Jira/Power BI; menos para Valeria (Notion). Reemplaza el "lo paso yo a Jira a mano". Absorbe "lo decidido viaja" y "traer Jira/Power BI adentro sin fricción".

### A4. Enlace estable por serie o equipo (`enlace-estable-por-serie`) — arreglar lo que existe
Notas de reunión y Whiteboard dejan de colgar del chat de una ocurrencia: viven en la serie o en el equipo, sobreviven a reprogramaciones y son buscables. Mecanismo: hacer menos doloroso lo nativo. Ataca solo la mitad "se pierde", no la calidad del registro. Para Valeria (variante tablero) y Paula. Reemplaza la captura de pantalla en Confluence. Absorbe "enlace estable".

### A5. Ritual de cierre con plantilla (`ritual-de-cierre`) — no es software nuevo
Plantilla de notas "Decisiones de hoy" (decisión · dueño · fecha · motivo) distribuida por IT como plantilla del tenant, más una práctica: los últimos 5 minutos el líder lee cada decisión en voz alta con dueño y fecha. Mecanismo: cambiar la regla con la herramienta que ya está. Ataca la ambigüedad y la gente que no participó; no ataca la reescritura. Para Valeria y Sofía. Reemplaza el cierre informal.

## Comparación

| Alternativa | Desirable | Feasible | Viable | Creencia más riesgosa |
|---|---|---|---|---|
| A1 cierre-confirmado | mixed — pain evidenced, relief not tested (`real` i1; `survey` Q9). Sofía y Martina lo piden con esas palabras: deseo declarado, no reacción | to check with tech — compliance/residencia acota dónde vive el registro | unknown — objeto exacto de la #1 del registro, sin evidencia; `secondary`: arriba se cobra control de IT | El líder confirma la lista en el momento, al final de la mayoría de las reuniones que deciden, y lo confirmado es lo que el equipo ejecuta |
| A2 recap-de-decisiones | mixed — evidencia de solución **en contra** de la versión actual: 6/10 corrigen o abandonan el recap (`real` i2); ~20 "con un pero" (`survey`). Prueba adopción de la mecánica, no confianza en la versión estructurada | to check with tech — recap y Live Share existen (`secondary`); leer Miro/Power BI/Slack como entrada es otra cosa | unknown, mejor señal del set: la IA es lo que el mercado cobra arriba (`secondary`). Sin voz de IT | La lista distingue decisión de comentario, con dueño y motivo, con precisión suficiente para que el líder la confirme sin reescribirla y no invente decisiones |
| A3 decision-al-ticket | mixed — pain evidenced (`real` i1/i5; `survey` Q4: 53% de artefactos preexisten). En contra: Valeria cierra en Notion; el recap pegado en el ticket "nadie lo leyó" | to check with tech — conectores por tenant; datos que salen de M365 | unknown / weak — el valor queda visible en Atlassian, no en el reporte de adopción de Teams (`assumption`, #10) | El destino es Jira/Confluence para la mayoría del segmento, IT permite el conector, y la decisión creada desde la reunión se lee ahí |
| A4 enlace-estable-por-serie | mixed — única con evidencia de solución positiva en sustituto cercano: la continuidad retiene a Tomás y Javier en Miro (`real` i3); 43% abandonó Whiteboard (`survey`). Necesaria, no suficiente | to check with tech — cambio de modelo, no de UI | weak — arreglo del plan base (`assumption`, coherente con `secondary`) | Con enlace estable, el líder vuelve a lo nativo y lo que queda ahí le evita la reescritura (i2 sugiere que no) |
| A5 ritual-de-cierre | mixed — pain evidenced; Paula valora las notas, Sofía y Tomás ya hacen parte del ritual (`real`); en contra: 31% no sabe que existen notas (`survey`), y se pierden al reprogramar (i3) | strong — nada que construir; distribución de plantilla por tenant to check with tech | weak — sin licencia que cobrar; retención si IT lo cuenta como adopción (`assumption`) | Los Team Leads sostienen un ritual de cierre de 5 minutos sin que el producto lo imponga, más de un mes |

Ninguna columna sale `strong`; las cinco desirables son `mixed` porque la evidencia es sobre el dolor. Las únicas reacciones reales a una solución son la negativa al recap actual (A2) y la positiva a la continuidad de Miro (A4).

## Decisión

Elegidas para testeo en paralelo **A1 cierre-confirmado** y **A2 recap-de-decisiones**, por el PM el 2026-10-06, coincidiendo con la recomendación. Razones: son el mismo registro con dos creencias asesinas independientes (conducta en A1, precisión en A2), cada una refutable barato y por separado; juntas sostienen la única historia de Max que la evidencia secundaria permite (estructura que nadie ofrece + IA bajo control de IT, que es lo que se cobra arriba). A3 y A4 no compiten: son niveles posteriores de lo mismo (a dónde se entrega, dónde vive). A5 es la versión sin software de la conducta de A1.

Cambiaría la decisión: telemetría que muestre que el recap se publica sin tocar (A2 pierde motivo → A1 sola); IT que no nombre un registro de decisiones frente a Compras (→ back-to-research); encuesta corta que muestre que el segmento cierra mayoritariamente en Jira (A3 sube a competir).

## A testear

Diseñado el 2026-10-06 en `product/tests/2026-10-06-2043-la-reunion-no-cierra.md` (`/design-solution-tests`):

- A1 — creencia #11 del registro (`[feature: cierre-confirmado] [value]`), **T1 `concierge`**: 5 Team Leads del pool, ~15 reuniones reales en 2 semanas; una persona del equipo redacta la lista al final y se mide si el líder la confirma antes de cortar (≥ 2/3) y si deja de reescribir al día siguiente (≥ 2/3). A5 `ritual-de-cierre` es el instrumento del test, no una rival.
- A2 — creencia #12 del registro (`[feature: recap-de-decisiones] [feasibility]`), **T2 `technical-test`**: sobre las reuniones grabadas de T1, con la lista confirmada como clave de respuestas; precisión ≥ 80%, cobertura ≥ 70%, decisiones inventadas en ≤ 2 de 10 reuniones, dueño ≥ 70%, y superar al recap genérico. La creencia de valor de A2 (el líder la confirma sin reescribir) es el siguiente paso si T2 pasa.

## Value proposition: A1 cierre-confirmado

- **Pain relieved:** los 20–60 min de reescribir a mano después de cada reunión y la ejecución errada cuando esa reescritura se demora o queda ambigua (`real`, i1: Andrés 4 días de cliente sin atención, Javier 2 semanas de dev).
- **Gain created:** Valeria sale de la reunión con lo decidido ya escrito, con dueño, fecha y motivo, visto por todos — incluidos los que no hablaron — y lo encuentra la semana siguiente en la misma serie.
- **Replaces:** el ticket a mano, el correo de cierre y el recap corregido; se cambia porque cuesta 3 minutos en vivo en vez de media hora después, y porque el equipo lee lo mismo que ella confirmó.
- **Deliberately does not:** no transcribe la reunión, no vota ni prioriza, no reemplaza Jira ni Notion como lugar de trabajo, no decide por el líder.

## Value proposition: A2 recap-de-decisiones

- **Pain relieved:** los 10–30 min de corregir o reescribir un recap que nivela todo, no asigna dueño y no ve el artefacto, y la decisión inventada que el equipo ejecuta (`real`, i2: Paula, una semana de dos devs).
- **Gain created:** Valeria recibe una lista corta ya armada —qué se decidió, quién, cuándo, por qué, con la votación del tablero o el filtro del dashboard como fuente— y solo tiene que confirmarla o tocar una línea.
- **Replaces:** el recap de dos páginas que hoy se corrige o se abandona; se cambia porque el trabajo de separar decisión de comentario lo hace la máquina y el líder solo valida.
- **Deliberately does not:** no publica sin confirmación del líder, no resume la conversación entera, no lee artefactos fuera del perímetro que IT permita.

## Beliefs

- `[opportunity: la-reunion-no-cierra] [value]` — referenciada, #2 del registro.
- `[opportunity: la-reunion-no-cierra] [viability]` — referenciada, #1 del registro.
- `[feature: cierre-confirmado] [value]` Si al final de una reunión que decide se le ofrece al líder una lista corta decisión · dueño · fecha · motivo, la confirma en el momento en la mayoría de los casos y el equipo ejecuta lo confirmado; deja de reescribir después. *(registrada el 2026-10-06 como #11; en testeo, T1)*
- `[feature: cierre-confirmado] [usability]` Confirmar la lista toma al líder menos de 5 minutos al final de la reunión y no alarga reuniones ya consideradas largas (26% de quejas). *(propuesta — se prueba con prototipo; T1 captura la duración del cierre como dato)*
- `[feature: recap-de-decisiones] [feasibility]` Una lista decisión · dueño · fecha · motivo generada a partir de la transcripción y de lo ocurrido en el artefacto compartido distingue decisión de comentario, asigna dueño y motivo, y no inventa decisiones, con precisión suficiente para que el líder la confirme sin reescribirla. *(registrada el 2026-10-06 como #12; en testeo, T2 — era la "creencia más riesgosa" de la tabla, antes redactada como de valor)*
- `[feature: recap-de-decisiones] [value]` Una lista generada a partir del audio y del artefacto, con dueño y motivo, la confirma el líder sin reescribirla en la mayoría de las reuniones; hoy 6/10 corrigen o abandonan el recap. *(propuesta — siguiente paso si T2 pasa, Wizard of Oz)*
- `[feature: recap-de-decisiones] [feasibility]` Es posible tomar como entrada lo que ocurrió en el artefacto compartido (nativo y, vía Live Share, de terceros) dentro de las restricciones de compliance y residencia de datos del segmento. *(propuesta — to check with tech)*
- `[feature: recap-de-decisiones] [viability]` IT de una cuenta grande nombra el recap estructurado bajo su control como capacidad de Max frente a Compras; el recap genérico no. *(propuesta — refina la #1 del registro, se resuelve con la entrevista a IT)*

Registradas en `product/overview.md` el 2026-10-06 las dos en testeo (#11 y #12); las demás `[feature]` siguen pendientes de registro. Nada de A3–A5.

## Discarded or parked

- A3 decision-al-ticket — parked: no compite con A1, es su nivel de entrega; vuelve al plan de exposición cuando A1 sobreviva el test, o antes si la encuesta corta muestra que el segmento cierra mayoritariamente en Jira/Confluence.
- A4 enlace-estable-por-serie — parked: necesaria, no suficiente; es un prerequisito de A1 (el registro vive en la serie) y entra como requisito, no como alternativa. Vuelve sola si tech dice que atar el registro a la serie no es viable.
- A5 ritual-de-cierre — parked: comparte la creencia de conducta con A1; es el instrumento del test T1 de A1 (concierge con plantilla), no una rival.
- Participación silenciosa / votar con límite por persona — parked: ataca el insight 4 (participación), no el cierre. Vuelve si el test de A1/A2 muestra que la decisión no queda bien porque nunca se tomó con claridad.
- Señalar sobre la pantalla compartida / misma vista para datos — parked: ataca el insight 5, otro problema; candidata a oportunidad propia.
- "Herramientas colaborativas integradas", editar un documento entre varios, votar o priorizar en vivo (heredadas) — discarded para esta oportunidad: colaboración en vivo, que el mercado regala (`secondary`) y que la mitad del corpus dice no necesitar (`real`, i5).

## Outcome
(lo agrega /analyze-solution-tests)
