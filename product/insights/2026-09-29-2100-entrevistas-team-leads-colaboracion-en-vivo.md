---
source: real
sources:
  - product/interviews/2026-09-25-1000-tomas-aguirre.md
  - product/interviews/2026-09-25-1100-andres-quintero.md
  - product/interviews/2026-09-25-1600-lucia-fernandez.md
  - product/interviews/2026-09-28-0900-javier-molina.md
  - product/interviews/2026-09-28-0930-martina-rojas.md
  - product/interviews/2026-09-28-1000-diego-paredes.md
  - product/interviews/2026-09-28-1200-sofia-martinez.md
  - product/interviews/2026-09-28-1400-paula-benitez.md
  - product/interviews/2026-09-28-1500-valeria-castro.md
  - product/interviews/2026-09-28-1700-ricardo-salinas.md
guide: product/interview-guides/2026-09-23-2030-colaboracion-en-vivo-fuera-de-teams.md
opportunity: trabajo-en-vivo-fuera-de-teams
n: 10 entrevistas de exploración (26–34 min), Team Leads de SaaS B2B de 650–2.000 empleados, 6 países
date: 2026-09-29
---

# Insights: entrevistas a Team Leads sobre colaboración en vivo en reuniones de más de 5 personas

## Corpus y límites

10 entrevistas reales, todas reclutadas desde la encuesta del 23/09 (respondentes R-024 a R-224, 6 por panel y 4 por email). Roles: 4 Engineering Managers, 2 Product Leads, 1 Design Lead, 1 Data Team Lead, 1 Head of Support Ops, 1 Director de Plataforma. Reuniones analizadas: retros (2), PI/planning (3), priorización de incidencias/escalamientos (2), revisión de métricas (1), revisión de PRD (1), syncs informativos (2).

Sesgos a tener en cuenta: todos conducen reuniones en Teams por decisión de IT (ninguno eligió la herramienta); ninguno tiene rol de IT ni de compras, así que **estas entrevistas no dicen nada sobre las creencias de viabilidad** (#2, #5, #8 del overview). Un entrevistado (Tomás) corrigió su respuesta de encuesta: "salgo de Teams en todas" era exagerado. Dos (Paula, Ricardo) sostienen que en reuniones de 14–16 personas no se decide y no debe decidirse.

Las herramientas por las que salen se reparten igual que en la encuesta: **donde ya vive el trabajo** (Jira: Tomás, Martina · Excel/SharePoint: Andrés · Power BI: Diego · Confluence: Sofía · Figma: Valeria) contra **tablero creado para la sesión** (Miro: Tomás, Javier · FigJam: Valeria · Google Doc desechable: Sofía). Lucía y Paula se quedan dentro (Whiteboard y notas nativas); Ricardo no usa nada.

---

## 1. La reunión no falla al colaborar sino al cerrar: la decisión no queda con dueño, fecha y razón, y se ejecuta mal

**Recurre en 9 de 10 entrevistas.** Es el hallazgo más fuerte del corpus y el único que atraviesa todas las variantes (tablero, backlog, datos, documento, solo voz). En todos los casos la decisión sí se tomó en la reunión; lo que falló fue el tramo entre "quedó decidido" y "alguien lo ejecuta": el líder la reescribe a mano después (entre 20 y 60 minutos por reunión, siempre él y nadie más), y cuando esa reescritura se demora, se pierde o queda ambigua, el equipo ejecuta otra cosa. Los costos contados son concretos: un cliente 4 días sin atención, una campaña 3 días con presupuesto de más, dos semanas de desarrollo descartadas, una semana de un diseñador en algo ya descartado, una semana de dos devs en una idea que nunca se aprobó, una migración de bases al revés con guardia de fin de semana. Implicación: el producto no necesita un mejor lienzo, necesita un **cierre de reunión** que capture cada decisión con dueño, fecha y motivo en el momento, visible para todos (incluidos los que no hablaron) y enlazado al artefacto donde después se trabaja (Jira, Confluence, el ticket).

> Evidence: "Lo paso yo a Jira, a mano. Creo un ticket por acuerdo, con responsable, y le pego el link del frame. Me lleva unos veinte minutos [...] Nadie más lo hace." — Tomás Aguirre
>
> "En mi correo quedó, pero el líder de Ecuador entendió que lo pasaba yo, y yo entendí que lo pasaba él. Nadie lo pasó. [...] El cliente esperó cuatro días." — Andrés Quintero
>
> "El equipo de México leyó el recap, no el hilo, y entendió que no era prioridad. Entregaron dos semanas tarde. [...] Desde entonces, después de cada planning, reescribo el recap. Media hora." — Javier Molina
>
> "El qué queda en Jira. El problema es el por qué. [...] Un mes después [...] nadie se acordaba. Ni yo, y eso que la decidí yo. Se reabrió la discusión entera." — Martina Rojas
>
> "Lo que nos falla es cómo se cierra la reunión: que quede claro qué se decidió, que lo sepan todos, incluso los que no hablaron. Eso lo hago medio a mano y a veces se me va." — Sofía Martínez
>
> "Se habló en la sync, cada uno se fue con su versión y nadie lo escribió. Yo pensé que el arquitecto iba a hacer el ADR y él pensó que yo lo iba a mandar por correo." — Ricardo Salinas

---

## 2. El recap de IA se usa, pero no sirve como registro: nivela todo, no ve lo que pasó en el artefacto y a veces inventa decisiones

**Recurre en 6 de 10** (Lucía, Javier, Martina, Diego, Paula, Valeria). Responde al "por qué abierto" de la encuesta. Los líderes lo probaron y lo describen con precisión: resume la conversación al mismo nivel sin distinguir decisión de comentario (Javier, Martina); no distingue quién se comprometió a qué (Lucía); no ve lo que pasó fuera del audio, es decir la votación en el tablero, el filtro del dashboard, el hilo de Slack donde quedó la razón (Valeria, Diego, Martina); y en el peor caso convierte una idea en decisión y el equipo la ejecuta (Paula: una semana de dos devs). El resultado es que quien lo usa lo corrige a mano (Paula, 10 min por reunión) o lo abandona (Martina, tras dos intentos). Implicación: el recap tiene que producir una **lista corta y estructurada** (decisión · dueño · fecha · motivo), pedir confirmación explícita del líder antes de publicarse, y tomar como entrada lo que ocurrió en el artefacto compartido, no solo la transcripción.

> Evidence: "El recap resume todo al mismo nivel. Dos páginas. No distingues qué se decidió de qué se comentó." — Javier Molina
>
> "Me resumió la conversación, no las decisiones. Tenía un párrafo sobre la discusión de las seis historias, pero no decía cuál entró y por qué. [...] La primera vez lo pegué en el ticket. Nadie lo leyó, era largo. La segunda ni lo abrí." — Martina Rojas
>
> "Marca como decisión cosas que eran solo ideas. Alguien dice 'podríamos pasar el release al 20' y en el resumen aparece 'se decidió pasar el release al 20'. [...] Perdimos más o menos una semana de dos desarrolladores." — Paula Benítez
>
> "No ve lo que pasó en el FigJam, solo lo que se habló. Y como la votación fue en el tablero, el resumen decía algo como 'se discutieron prioridades'. Pues sí, gracias." — Valeria Castro
>
> "Dice 'se revisaron las ventas de Chile' y no dice con qué filtro ni qué gráfico. Entonces igual tengo que hacer el correo." — Diego Paredes

---

## 3. Whiteboard y las notas nativas se pierden cuando cambia la convocatoria; eso, más que la falta de funciones, es lo que expulsa a Miro

**Recurre en 6 de 10.** Cinco líderes probaron la pizarra de Teams y la abandonaron (Tomás, Lucía, Javier, Sofía, Ricardo); Paula sufre lo mismo con las notas. Las razones funcionales coinciden con la encuesta (sin votación, sin plantillas ni agrupado, lenta con 10+ personas), pero el motivo de abandono definitivo es otro: **el artefacto queda atado al chat de una ocurrencia de la reunión** y desaparece cuando se recrea la serie, se reprograma por un feriado o se convoca una segunda sesión. Tres líderes perdieron acuerdos así; dos (Lucía, Sofía) ahora sacan capturas de pantalla y las pegan en Confluence como único registro fiable. En contraste, lo que retiene a Tomás y Javier en Miro es exactamente la continuidad: un tablero por trimestre, un frame por sesión, la retro anterior a la vista. Implicación: antes que agregar funciones, la pizarra y las notas necesitan **un enlace estable por equipo o por serie** que sobreviva a reprogramaciones y sea buscable; después, votación con límite por persona, plantillas y rendimiento con 10–15 editores.

> Evidence: "A las dos semanas, para la retro siguiente, fui a buscarla y no estaba. Quedó colgada del chat de esa reunión, y justo en el medio se había recreado la serie [...] Busqué como quince minutos. Perdí los acuerdos, así de simple." — Tomás Aguirre
>
> "Resulta que queda atada al chat de esa reunión, y como la segunda sesión fue una convocatoria nueva, pues ahí no aparecía. [...] Desde entonces hago captura de pantalla al terminar y la pego en Confluence. Es cutre, pero es lo único que sé que voy a encontrar." — Lucía Fernández
>
> "Movimos el review un día por un feriado en Brasil, se creó otra invitación y las notas quedaron en la otra, en la original. Media hora antes estaba yo buscando dónde había quedado la agenda." — Paula Benítez
>
> "Yo tengo un solo tablero por trimestre. Cada retro es un frame nuevo, al lado de la anterior. [...] Esa continuidad es la razón por la que estamos en Miro." — Tomás Aguirre

---

## 4. Quien queda mirando la pantalla de otro no opina, y sus objeciones aparecen semanas después

**Recurre en 7 de 10.** En casi todas las reuniones hay 1–3 personas que no entran al artefacto: invitados sin licencia (Tomás, Javier), cuentas personales de Google que el tablero no reconoce (Valeria), sin permiso en Confluence (Sofía), laptop de 13" donde las notas son "puntitos" (Lucía, Javier), o simplemente un rol que no toca (Andrés, Martina). Todas resuelven igual: esa persona dicta por chat o voz y el líder transcribe. Lo que los líderes señalan como más grave no son los minutos sino que **esa gente no participa en la decisión**: la objeción de soporte sobre WhatsApp salió una semana después en un café; un dev discrepó por privado después de cerrado el planning; los nuevos "votan cuando pregunto, pero opinar, poco". Se agrava con votaciones poco fiables: contar manos y pulgares de 9–16 personas (Lucía, Andrés, Ricardo) o stickers sin límite por persona que obligan a recontar a mano (Valeria). Implicación: un mecanismo de **participación silenciosa dentro de la llamada** (votar con límite por persona, marcar acuerdo/desacuerdo, escribir sin acceso al artefacto externo) resuelve a la vez el acceso y la inclusión, y da al líder un conteo en el que confíe.

> Evidence: "Nunca logró entrar [...] se quedó mirando mi pantalla compartida. No dijo casi nada. Y lo peor es que después, como a la semana, me la encuentro en un café [...] y me dice que no estaba de acuerdo con sacar la reprogramación de citas por WhatsApp. Una objeción importante." — Valeria Castro
>
> "Nico, uno de Montevideo, me escribe sus notas por el chat de Teams y yo se las paso al tablero. Me dicta, literalmente." — Tomás Aguirre
>
> "Contar reacciones de nueve personas con la mitad sin cámara... a ver, funciona, pero no te fías del todo del número." — Lucía Fernández
>
> "No hay forma de que cada uno marque su prioridad sin que se transforme en conversación. [...] Al final decidí yo. Y dos devs se quedaron con cara de no." — Martina Rojas
>
> "La gente que no entra al tablero no es poca. En casi todas hay alguien mirando desde afuera, y esa gente no opina. Eso me preocupa más que los minutos." — Valeria Castro

---

## 5. Cuando el trabajo vive en Jira, Excel, Power BI o Figma, nadie quiere otra herramienta: quieren señalar sobre la pantalla compartida

**Recurre en 5 de 10** (Tomás, Andrés, Diego, Valeria; Martina con la variante "todos editando es un caos"). Es la mitad del corpus que la encuesta llamó "integración" y confirma su lectura: estos líderes dicen explícitamente que no les falta nada en Teams y que mover el trabajo a otro lado sería doble trabajo. Su fricción es una sola, repetida en cada reunión: **nadie puede apuntar** sobre la pantalla compartida ("la de abajo, no, la otra, la del label rojo"). No es solo tiempo: Andrés cerró el ticket equivocado y el cliente recibió la notificación de cierre; Diego pasó 10–15 minutos con nueve personas discutiendo números distintos porque cada uno tenía otro filtro. Implicación: para esta variante la oportunidad no es un lienzo ni una app embebida sino **señalar y seleccionar en la pantalla compartida** (puntero de cada participante, "esta fila", "este gráfico") y, para datos, una forma de forzar que todos vean la misma vista. Es la variante que menos compite con Miro y la que más se parece a una mejora del compartir pantalla, que ya usa el 67%.

> Evidence: "Si pudieran apuntar con algo, me dirían 'esta' y listo. Pero no, todo pasa por mí. [...] Cerré un ticket que no era. [...] Al cliente le llegó la notificación de cierre y el caso seguía abierto." — Andrés Quintero
>
> "Alguien dice 'la de abajo', 'no, la otra', 'la que tiene el label rojo', y yo con el mouse dando vueltas. Perdemos un rato largo en eso, en serio." — Tomás Aguirre
>
> "Uno decía 'las ventas bajaron ocho por ciento' y otro 'no, a mí me sale que subieron'. Y estábamos hablando de números distintos sin darnos cuenta. Así estuvimos unos diez, quince minutos." — Diego Paredes
>
> "No veo para qué querría otra herramienta. Tengo Jira, tengo Grafana, tengo Miro para la retro. Lo que sí me serviría es algo que cierre la reunión con lo decidido y el por qué, y que eso quede en el ticket." — Martina Rojas

---

## Señales secundarias (no llegan a insight, pero pesan para el alcance)

- **Compliance retiene dentro de Teams y no es preferencia.** Lucía (pagos, España): herramientas externas prohibidas con datos de clientes, aprobar una nueva "son meses", "necesito que lo nativo funcione mejor". Un solo caso, pero es la voz del segmento que la creencia #3 supone; la encuesta ya había visto 5 menciones espontáneas.
- **Dos líderes rechazan decidir con más de 10 personas** (Paula, Ricardo): las decisiones "de verdad" se toman en llamadas de 3–4 después. Para ellos votar con 15 "es dar la sensación de que todos participaron". Segmento que no compra colaboración en vivo pero sí un cierre que registre lo que sí se decidió y lo que se derivó a otra reunión.
- **Descubrimiento de lo nativo sigue bajo**: Andrés vio notas de reunión por primera vez en la reunión de otra persona ("¿eso lo tiene Teams?"); Valeria no sabía que Teams tiene pizarra; Ricardo no sabía que se pueden embeber apps; Lucía tardó tres intentos en encontrar el botón. Coincide con el 31–40% de la encuesta.
- **El costo de acceso existe solo cuando hay mezcla de licencias o cuentas** (Tomás 5–7 min, Javier "diez largos", Valeria 6–8) y desaparece con SSO (Martina, Diego, Sofía: "en un minuto ya estábamos"). Javier añade un costo que la encuesta no midió: **saltar entre ventanas durante toda la reunión** ("el acceso es al principio; perder el hilo cada vez que cambias de herramienta es durante las dos horas").
- **El tablero creado para la sesión no se retoma** (Valeria: nadie lo abrió después; Sofía: el Google Doc del kickoff "queda por ahí"): confirma el 31% de Miro descartado de la encuesta y sugiere que es desechable por diseño, no perdido, siempre que lo decidido haya migrado a Jira o Confluence.

## Contraste con las creencias del overview

Ver conversación del 2026-09-29; las anotaciones se aplican en `product/overview.md` solo con aprobación.
