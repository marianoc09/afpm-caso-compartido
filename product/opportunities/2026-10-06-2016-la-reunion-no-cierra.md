---
status: framed
segment: Team Lead de una cuenta de más de 1.000 licencias de Microsoft 365 que conduce reuniones de 5 o más participantes en las que se toman decisiones — salga o no de Teams durante la llamada
personas: valeria-ortiz (primary, lo sufre), gustavo-ferreyra (secondary, lo sufre en variante datos), lucia-benitez (tertiary, lo paga), tomas-iriarte (negative, lo padece como efecto)
supersedes: product/opportunities/2026-09-15-2150-trabajo-en-vivo-fuera-de-teams.md
---

# Opportunity: La reunión no cierra

El Team Lead de una cuenta grande que decide en reuniones de 5+ paga el cierre con 20 a 60 minutos de reescritura manual por reunión (siempre él, nadie más) y, cuando esa reescritura se demora, se pierde o queda ambigua, el equipo ejecuta otra cosa — un cliente 4 días sin atención, dos semanas de desarrollo descartadas, una migración al revés; el momento es ahora porque el recap de IA que ya se paga no sirve como registro (6/10 lo corrigen o lo abandonan), porque el mercado está regalando la colaboración en vivo y cobrando el control sobre ella, y porque CollabCon, a mediados de febrero, fija la fecha para decidir qué mostrar.

## Segmento y personas

- **Valeria Ortiz (primary) — lo sufre.** ~40 min/semana reescribiendo notas en Notion; media hora para reconstruir "por qué decidieron esto". En las entrevistas, su variante (tablero creado para la sesión) es la que además pierde el artefacto nativo al cambiar la convocatoria.
- **Gustavo Ferreyra (secondary) — lo sufre, variante datos.** Su cierre es el correo con "qué filtro y qué gráfico se miró" (Diego: "dice 'se revisaron las ventas de Chile' y no dice con qué filtro; igual tengo que hacer el correo"). Cualquier lectura del problema que solo cubra tableros lo deja afuera.
- **Lucía Benítez (tertiary) — no lo sufre, lo paga.** Reporte de adopción de Premium frente a Compras, auditoría de herramientas no sancionadas. Es quien responde la creencia de viabilidad.
- **Tomás Iriarte (negative) — no lo sufre como costo, lo padece como efecto.** Es quien ejecuta la versión equivocada o discrepa por privado después de cerrado el planning. Sigue excluido como segmento; sirve como señal de consecuencia, no como usuario.
- **Persona faltante:** el Team Lead que **no decide con 10+** (2/10 entrevistas: Paula, Ricardo — "las decisiones de verdad se toman en llamadas de 3–4 después") y solo pide que quede registrado qué se decidió y qué se derivó. Ninguna persona sintética lo cubre; `/generate-personas` para ese rol cuando la agenda lo pida.

## Señales

| Señal | Procedencia | Fuente |
|---|---|---|
| 9/10 Team Leads reescriben a mano lo decidido después de cada reunión (20–60 min, siempre el líder); 6 cuentan ejecuciones erradas con costo concreto (cliente 4 días sin atención, 2 semanas de dev descartadas, campaña 3 días con presupuesto de más, migración al revés) | real | product/insights/2026-09-29-2100-entrevistas-team-leads-colaboracion-en-vivo.md, insight 1 |
| 6/10 usan el recap de IA y lo corrigen (10 min/reunión) o lo abandonan: nivela decisión y comentario, no asigna dueño, no ve lo que pasó en el artefacto, convierte ideas en decisiones | real | ídem, insight 2 |
| 5/10 probaron Whiteboard y lo abandonaron; el motivo definitivo es que el artefacto queda atado al chat de una ocurrencia y desaparece al recrear la serie o reprogramar; dos sacan capturas de pantalla como único registro fiable | real | ídem, insight 3 |
| 7/10: 1–3 personas quedan mirando la pantalla de otro y no participan de la decisión; las objeciones aparecen semanas después | real | ídem, insight 4 |
| 5/10 salen a donde ya vive el trabajo (Jira, Excel, Power BI, Confluence, Figma), dicen que no les falta nada en Teams y su fricción es señalar sobre la pantalla compartida | real | ídem, insight 5 |
| 24% de las decisiones tomadas afuera no queda registrada; 23% queda en Slack/WhatsApp; ~20 respondentes usan el recap de Copilot como registro "con un pero" | survey | product/insights/2026-09-29-2037-colaboracion-en-vivo-fuera-de-teams.md (n=182 que salen; n=210 total) |
| "Registro y continuidad entre reuniones" es el tema #1 de la abierta (31/95); "converger y decidir" el #2 (14/95) | survey | ídem, Q11 |
| Actividad #1 fuera de Teams: votar o priorizar (40%); anotar decisiones 33% | survey | ídem, Q5 |
| Costo de entrada ≥5 min solo en el 18% de reuniones internas (62% con externos, n=39 direccional) | survey | ídem, Q6 — **refuta** el "5 minutos por reunión" del brief anterior |
| Notas de reunión: 31% no sabía que existían, 28% las conoce y nunca las usó; Whiteboard: 43% la usó y dejó de usarla | survey | ídem, Q10 |
| Compliance o normativa europea aparece 5 veces sin preguntarlo como razón para quedarse dentro de Teams | survey | ídem, insight 6; + Lucía F. en entrevistas |
| La colaboración en vivo básica es plan base o medio (Zoom Basic, Meet Business Standard); lo que se cobra arriba es control de IT e IA (Teams Premium USD 10); Meet con Gemini apuesta a notas y "próximos pasos" post-reunión | secondary | product/research/2026-09-16-1313-colaboracion-en-vivo-dentro-de-la-videollamada.md |
| Ningún jugador publica adopción de colaboración en vivo; nadie reclama "decisiones con dueño" como capacidad | secondary | ídem |
| "Colaboración durante reuniones" fue la 3.ª categoría del portal de feedback (4.700 solicitudes); uso de notas 8%; quejas por colaboración en reunión 19–22% | real / unverified | Portal de feedback y telemetría (aportados por el PM); brief del caso sin fuente nombrada |
| En renovaciones de cuentas grandes, "colaboración" aparece en las conversaciones sobre Max | unverified | Ventas; sin registro de cuántas veces |
| Valeria ~40 min/semana en Notion; Gustavo ~10 min/reunión con el dashboard; Lucía 14 suscripciones a Miro/Notion en tarjetas corporativas | synthetic | product/personas/ |

Las señales `real` prueban que el costo existe y cómo se paga; todavía no dicen **cuán extendido** está en el segmento (10 entrevistas, sin n) ni **si IT lo nombraría** frente a Compras (ninguna entrevista fue a IT).

## Resultado de negocio

Comercial. **Upgrade a Max** (hoy 2,4% de las cuentas sube de plan; USD 8 por usuario por mes), con la retención (3,6% baja o no renueva; "pagamos por funciones que no usamos") como efecto secundario. La hipótesis de valor para Max no es "colaborar en vivo" — el mercado lo regala — sino un **cierre de reunión con rastro auditable bajo control de IT**, que IT pueda nombrar en el reporte de adopción que muestra al CFO. La entrevista a IT decide si el outcome es upgrade o solo retención.

## Restricciones

- Presupuesto máximo: USD 5M.
- CollabCon a mediados de febrero de 2027 (~4 meses). Fija la fecha de las decisiones de la agenda, no el alcance.
- Límites para cualquier solución: facilidad de uso, accesibilidad, compatibilidad con Microsoft 365, privacidad y seguridad corporativas, tiempo real, impacto mínimo en el rendimiento de la reunión.
- **Nuevo:** un registro de decisiones guarda nombres, compromisos y motivos; compliance (pagos, EEE — Lucía F., R-173, R-190) y residencia de datos acotan dónde puede vivir y quién lo puede leer.
- Contexto de compra: contrata y despliega IT; el Team Lead no elige. El valor tiene que ser visible en los reportes de adopción de IT.

## Creencias

Referencian `product/overview.md`, el único registro.

- `[opportunity: la-reunion-no-cierra] [value]` El Team Lead de cuenta grande que decide en reuniones de 5+ paga el cierre con 20–60 min de reescritura manual por reunión (siempre él) y con ejecuciones erradas cuando se demora; ese costo es general en el segmento — no un rasgo de los 10 entrevistados — y lo paga aunque no salga de Teams, porque el recap de IA y las notas nativas no le sirven como registro (nivelan decisión y comentario, no ven el artefacto, se pierden al cambiar la convocatoria). *(registrada el 2026-10-06 como #2; hereda la mitad confirmada de la antigua #1)*
- `[opportunity: la-reunion-no-cierra] [viability]` IT de una cuenta grande paga Max por un cierre de reunión con rastro auditable (decisión · dueño · fecha · motivo, enlazado al artefacto, bajo compliance) y lo puede nombrar frente a Compras en el reporte de adopción; la colaboración en vivo por sí sola no. *(registrada el 2026-10-06 como #1; refina la de "colaborar en vivo bajo control de IT")*
- Relacionadas ya registradas (numeración del registro al 2026-10-06): #4 — IT reconoce la capacidad frente a Compras y la fuga pesa en la renovación; #5 — "colaborar en vivo bajo control de IT"; #9 — el Team Lead cambiaría cómo cierra sus reuniones (confirmada por entrevistas); #10 — IT sube a Max si ve adopción visible de los Team Leads.
- Cerradas por este re-encuadre: #3 `[opportunity: trabajo-en-vivo-fuera-de-teams] [value]` (resolved: split — la mitad de minutos refutada, la de rastro heredada por la [value] nueva); #6 de producto queda `contradicted`.

## Agenda de investigación

Ordenada por costo. CollabCon como fecha límite dura; la decisión de pasar a `/explore-solutions` tiene que tomarse a fines de noviembre para llegar con 2,5 meses.

| Creencia | Instrumento | Decisión que destraba | Para cuándo |
|---|---|---|---|
| [value] — extensión del costo | **Datos propios**: en el segmento, cuántas reuniones recurrentes recrean la serie o la invitación (proxy de notas/Whiteboard perdidas); cuántas notas de reunión se editan *después* de terminar la llamada y por quién; uso del recap de Copilot y tasa de edición manual post-recap | Si el recap se publica sin tocar y las series no se recrean, el costo de cierre es menor de lo que dicen 10 entrevistas; si no, confirma con n de telemetría | 2 semanas (20 de octubre) |
| [viability] — qué cobra el mercado por "decisiones" | `/research-market` acotado: cómo Zoom AI Companion, Gemini "next steps" y Copilot recap tratan decisión/dueño/fecha, en qué plan, y si alguien vende "registro auditable de decisiones" a IT | Decide si el cierre con rastro puede vivir en Max o si ya es commodity de los recaps de IA | 2 semanas (20 de octubre) |
| [value] — cuántos, cuánto | `/design-survey` corta al pool de 210 (y panel nuevo): minutos de cierre por reunión, quién lo hace, dónde queda, ejecuciones erradas en el último trimestre, uso y corrección del recap; corrige Q9 (agrega "recap de IA") | Reemplaza el 20–60 min de 10 entrevistas por un número con n; dimensiona el segmento que decide en 5+ | 5 semanas (10 de noviembre) |
| [viability] — la voz de IT | `/design-interview` con responsables de Collaboration Services (perfil Lucía) de cuentas grandes: cómo justifican Max, si "registro auditable de decisiones" es algo que nombrarían frente a Compras, qué reporte de adopción los convencería, qué les impone compliance | Decide si el outcome es upgrade o solo retención, y qué debe medir cualquier solución para que IT lo vea. Era la fila pendiente del brief anterior; sigue sin hacerse | 7 semanas (24 de noviembre) |
| [value] — el porqué (persona faltante) | `/design-interview` corta a Team Leads del pool que **no** deciden con 10+ (Paula, Ricardo y afines) | Decide si la oportunidad incluye "qué se derivó a otra reunión" o solo "qué se decidió"; alimenta `/generate-personas` | 7 semanas (24 de noviembre) |
| Compuerta | Con los cuatro anteriores: `/explore-solutions` sobre esta oportunidad | Cierra o descarta; si cierra, 2,5 meses para CollabCon | Fines de noviembre |

## Ideas candidatas (no evaluadas)

Son el punto de partida de `/explore-solutions`, no una lista corta. Evaluadas el 2026-10-06 en `product/solutions/2026-10-06-2035-la-reunion-no-cierra.md` (status: testing-several); resultado por idea al final de cada línea.

- **Cierre de reunión estructurado** → `chosen` como A1 `cierre-confirmado` (en testeo) — lista corta decisión · dueño · fecha · motivo, confirmada explícitamente por el líder antes de publicarse, visible para todos (incluidos los que no hablaron). Implicación de los insights 1 y 2.
- **Recap que lea el artefacto, no solo el audio** → `chosen` como A2 `recap-de-decisiones` (en testeo) — la votación en el tablero, el filtro del dashboard, el hilo donde quedó la razón, como entrada del resumen. Insight 2.
- **Lo decidido viaja al lugar donde vive el trabajo** → `parked` como A3 `decision-al-ticket` (nivel de entrega de A1) — Jira, Confluence, el ticket — en vez de quedar en el chat de la reunión. Insights 1 y 5; cruza con la idea "traer Miro/Jira/Power BI adentro" del brief anterior.
- **Enlace estable por equipo o por serie** → `parked` como A4 `enlace-estable-por-serie` (prerequisito de A1, no rival) — para notas y Whiteboard, que sobreviva a reprogramaciones y sea buscable. Insight 3 — lo que retiene a Tomás y Javier en Miro.
- **Participación silenciosa dentro de la llamada** → `parked` (ataca el insight 4, no el cierre) — votar con límite por persona, marcar acuerdo/desacuerdo, escribir sin acceso al artefacto externo. Insight 4.
- **Señalar y seleccionar sobre la pantalla compartida** → `parked` (insight 5, candidata a oportunidad propia); para datos, forzar que todos vean la misma vista. Insight 5, variante Gustavo. Es la que menos compite con Miro.
- **Registro de "qué se derivó a otra reunión"** → `chosen` absorbida en A1 como campo — para quien no decide con 10+. Señal secundaria (Paula, Ricardo).
- Heredadas del brief anterior → `discarded` para esta oportunidad (colaboración en vivo que el mercado regala y que la mitad del corpus no pide); "traer herramientas externas adentro" se absorbe en A3: "herramientas colaborativas integradas"; editar un documento entre varios; votar o priorizar en vivo; traer herramientas externas adentro sin fricción de enlaces y permisos.
