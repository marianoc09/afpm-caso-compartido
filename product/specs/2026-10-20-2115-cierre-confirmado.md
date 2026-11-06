---
feature: cierre-confirmado
opportunity: la-reunion-no-cierra
solutions: product/solutions/2026-10-06-2035-la-reunion-no-cierra.md
tests: product/tests/2026-10-06-2043-la-reunion-no-cierra.md
personas: valeria-ortiz (primary), gustavo-ferreyra (secondary)
status: draft
date: 2026-10-20
---

# Cierre confirmado

## Problem

El Team Lead de una cuenta grande que decide en reuniones de 5+ paga el cierre con 20–60 minutos de reescritura manual después de cada reunión —siempre él— y, cuando esa reescritura se demora o queda ambigua, el equipo ejecuta otra cosa: un cliente 4 días sin atención, dos semanas de desarrollo descartadas, una migración al revés. El recap de IA que ya se paga no sirve como registro (6/10 lo corrigen o abandonan) y las notas nativas se pierden al cambiar la convocatoria. El momento es ahora: el mercado regala la colaboración en vivo y cobra el control; nadie vende "decisiones con dueño"; CollabCon (febrero 2027) fija la fecha.

> Evidence: "Lo paso yo a Jira, a mano. Creo un ticket por acuerdo, con responsable [...] Me lleva unos veinte minutos. Nadie más lo hace." — Tomás Aguirre, product/insights/2026-09-29-2100-entrevistas-team-leads-colaboracion-en-vivo.md, insight 1
>
> Evidence: "En mi correo quedó, pero el líder de Ecuador entendió que lo pasaba yo, y yo entendí que lo pasaba él. Nadie lo pasó. El cliente esperó cuatro días." — Andrés Quintero, ídem
>
> Evidence: 24% de las decisiones sin registro; "registro y continuidad" tema #1 de la abierta — product/insights/2026-09-29-2037-colaboracion-en-vivo-fuera-de-teams.md, Q9/Q11 (survey)

## Who it's for

- **Valeria Ortiz (primary)** — conduce 6–8 reuniones semanales de 8+; cierra con un mensaje en el canal y reescribe en Notion (~40 min/semana); reconstruir "por qué decidieron esto" le lleva media hora.
- **Gustavo Ferreyra (secondary)** — variante datos: su cierre es el correo con "qué filtro y qué gráfico"; lo sirve si el campo *motivo* admite "con este filtro".
- Fuera: Tomás Iriarte (negative, padece el efecto, no es usuario) y Lucía Benítez (tertiary, lo paga; decide la viabilidad, no usa la función).

## User journey

1. **Trigger** — Valeria conduce el planning quincenal (12 personas, FigJam compartido). Faltan 5 minutos y ya se decidieron tres cosas y una quedó para otra reunión.
2. Teams le muestra, solo a ella, el panel lateral "Decidido hoy" con la lista decisión · dueño · fecha · motivo armada durante la reunión, más la línea "derivado a otra reunión". Los campos que no se dijeron están en blanco, marcados como pendientes.
3. Valeria lee la lista en voz alta, corrige una fecha, completa un dueño que faltaba, y confirma. Le toma menos de 3 minutos.
4. La lista confirmada se publica en el chat de la reunión para los 12 asistentes, hablaran o no, con su nombre y la hora de confirmación.
5. Al día siguiente no manda el mensaje al canal ni reescribe en Notion: copia el enlace de la lista confirmada donde lo necesita.
6. **Outcome** — Dos semanas después, en el siguiente planning de la misma serie (reprogramado por un feriado), abre "Decidido hoy" y ve la lista anterior. Cuando un stakeholder pregunta "¿por qué sacaron la reprogramación por WhatsApp?", el motivo está ahí, con la fecha y quién lo decidió. La reunión existió.

*Pasos 1–4 son la versión testeada en T1 (con una persona en lugar del panel); 5–6 son la implicación de los insights 1 y 3, no observados todavía.*

## Critical user stories

### Confirmar lo decidido antes de cortar

As Valeria Ortiz, I want ver y confirmar la lista decisión · dueño · fecha · motivo antes de que termine la llamada, so that lo decidido quede escrito en el momento y no tenga que reescribirlo después.

Acceptance criteria:
- [ ] Cinco minutos antes de la hora de fin prevista, o cuando el organizador lo pide, aparece el panel "Decidido hoy" solo para el organizador.
- [ ] El organizador puede confirmar tal cual, editar cualquier campo y confirmar, o posponer; cada acción queda registrada con hora.
- [ ] Confirmar una lista de 3 decisiones con un campo editado toma menos de 5 minutos de reloj.
- [ ] La lista incluye la sección "derivado a otra reunión", que puede confirmarse aunque no haya decisiones.
- [ ] Edge: si la llamada termina sin confirmación, la lista no se publica y queda como borrador visible solo para el organizador. No hay recordatorio automático.

Traces to: insight 1 (reescritura 20–60 min); señal secundaria Paula/Ricardo (qué se derivó); T1 S1.

### Los huecos quedan a la vista, no se inventan

As Valeria Ortiz, I want que un dueño, fecha o motivo que no se dijo quede en blanco y marcado, so that nadie ejecute una decisión sin dueño creyendo que lo tenía.

Acceptance criteria:
- [ ] Un campo no completado se muestra como "pendiente", nunca con un valor sugerido ni autocompletado.
- [ ] La lista se puede confirmar con huecos; la publicación muestra los huecos igual que el organizador los vio.
- [ ] El campo *motivo* acepta texto libre que puede referir al artefacto ("con filtro región = Chile, gráfico 3").
- [ ] Edge: una decisión sin dueño confirmada aparece destacada en la publicación como "sin dueño".

Traces to: insight 2 (el recap inventa decisiones; Paula, una semana de dos devs); insight 1 Andrés (dueño ambiguo); variante Gustavo/Diego.

### Todos leen lo mismo, incluidos los que no hablaron

As Valeria Ortiz, I want que la lista confirmada llegue a todos los asistentes de la reunión, so that quien quedó mirando la pantalla de otro sepa qué se decidió y objete ahora, no en un café una semana después.

Acceptance criteria:
- [ ] Al confirmar, la lista se publica en el chat de la reunión como un mensaje a nombre del organizador, con hora de confirmación.
- [ ] Todo asistente de la convocatoria la ve, tenga o no acceso al artefacto externo usado en la reunión.
- [ ] Después de confirmada, solo el organizador puede editarla; cada cambio queda en un historial visible para todos los asistentes.
- [ ] La publicación deja el texto en formato copiable (texto plano) para pegarlo en Jira, Notion o un correo.
- [ ] Edge: quien entró como invitado externo sin licencia ve la lista en el chat de la reunión mientras conserve acceso a ese chat.

Traces to: insight 4 (7/10: 1–3 personas no participan; objeción de Valeria C. una semana después); insight 1 Sofía ("que lo sepan todos, incluso los que no hablaron").

### Encontrarla en la próxima reunión de la serie

As Valeria Ortiz, I want que la lista confirmada viva en la serie o en el equipo, no en el chat de una ocurrencia, so that la encuentre dos semanas después aunque la reunión se haya reprogramado.

Acceptance criteria:
- [ ] Desde cualquier ocurrencia de la serie se accede a las listas confirmadas de las ocurrencias anteriores, en orden.
- [ ] Reprogramar, mover por feriado o recrear la serie no cambia dónde se encuentra la lista.
- [ ] La lista es buscable por texto en Teams (decisión, dueño, motivo).
- [ ] Edge: una reunión única (sin serie) guarda su lista en el equipo o canal del organizador.

Traces to: insight 3 (Tomás, Lucía, Paula: artefacto perdido al cambiar la convocatoria); persona Valeria (rastro disperso, media hora para reconstruir).

## Hypothesis

We believe los Team Leads de cuentas grandes que deciden en reuniones de 5+ will confirmar la lista "Decidido hoy" al final de la mayoría de sus reuniones que deciden, y dejar de producir un registro aparte al día siguiente, because hoy ese registro les cuesta 20–60 minutos y, cuando se demora, el equipo ejecuta otra cosa.

We're wrong if, en 4 semanas con 15–20 líderes y sin acompañante en la llamada, menos de 2/3 de las reuniones que deciden terminan con lista confirmada, o si en 1/3 o más de las confirmadas el líder produce al día siguiente un registro con contenido distinto.

## Detail decisions

Tomadas el 2026-10-20 por el PM, con la opción recomendada en los tres casos:

- **Dónde aparece:** panel lateral de la reunión solo para el organizador; la publicación es un mensaje en el chat de la reunión. (Alternativa no elegida: componente Loop editable en el chat.)
- **Quién edita después de confirmar:** solo el organizador, con historial de cambios visible para todos.
- **Si el líder pospone:** nada automático; el borrador queda visible solo para él y no se publica. (Alternativa no elegida: recordatorio único a las 24 h — agregaría una conducta que T1 no mide como mecanismo.)

## Alternatives considered

Explored in: product/solutions/2026-10-06-2035-la-reunion-no-cierra.md
- A2 recap-de-decisiones — en testeo en paralelo (T2); misma lista generada por la máquina, creencia independiente (precisión).
- A3 decision-al-ticket — parked: nivel de entrega de A1; vuelve si A1 sobrevive el test o si la encuesta muestra que el segmento cierra en Jira.
- A4 enlace-estable-por-serie — parked: prerequisito de A1 (historia 4), entra como requisito.
- A5 ritual-de-cierre — parked: instrumento del test T1, no rival.
- Participación silenciosa; señalar sobre la pantalla — parked: atacan otros insights.
- Colaboración en vivo heredada — discarded: el mercado la regala y la mitad del corpus no la pide.

## Tested before spec

Tested in: product/tests/2026-10-06-2043-la-reunion-no-cierra.md
- T1 cierre-confirmado (concierge) — not run al 2026-10-13 (campo 13–24 oct, seguimiento al 31 oct) · creencia #11 `[feature: cierre-confirmado] [value]`
- **riskiest belief not tested (declared)** — la spec se escribe antes del resultado por decisión del PM; la hipótesis queda abierta hasta `/analyze-solution-tests T1`.
- Esta spec mantiene la versión testeada: lista al final, el líder confirma, huecos en blanco, publicación a todos, atada a la serie. No cambia mecanismo, quién hace qué, conducta medida ni segmento.

## Assumptions

Referencian `product/overview.md`, el único registro.

- [feature: cierre-confirmado] [value] #11 — el líder confirma en el momento y deja de reescribir. *En testeo (T1).*
- [feature: cierre-confirmado] [usability] #13 — confirmar la lista toma menos de 5 minutos y no alarga reuniones ya consideradas largas (26% de quejas).
- [feature: cierre-confirmado] [feasibility] #14 — el registro puede vivir atado a la serie o al equipo, sobrevivir a reprogramaciones y ser buscable dentro de las restricciones de compliance y residencia de datos del segmento.
- [feature: cierre-confirmado] [value] #15 — la lista confirmada publicada en el chat alcanza para que quienes no hablaron se enteren y objeten antes de ejecutar.
- [opportunity: la-reunion-no-cierra] [viability] #1 — IT nombra el registro auditable frente a Compras. *Instrumento: entrevista a IT, 24 nov.*
