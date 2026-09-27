---
opportunity: trabajo-en-vivo-fuera-de-teams
beliefs: "#1 [opportunity: trabajo-en-vivo-fuera-de-teams] [value]; #4 [product] [value]"
status: draft
---

# Encuesta: trabajo en vivo fuera de Teams durante reuniones de 8+

- **Objetivos de aprendizaje:**
  - **G1 — Frecuencia y destino.** En qué proporción de sus reuniones de 8+ el grupo sale de Teams para trabajar sobre material, y hacia qué tipo de herramienta (tablero, backlog, documento o dashboard, que es la variante Gustavo). → Decide el tamaño del problema y si la variante "datos" entra en el alcance o queda como segmento aparte.
  - **G2 — Costo del desvío.** Minutos perdidos entre el enlace y el trabajo, qué los causa (permisos, licencias) y cuánto tiempo semanal se va en reconstruir el resultado. → Si el costo es bajo, la oportunidad se achica a "rastro disperso" (cruza con la creencia #7). Reemplaza el 22% de la encuesta post-reunión, que no tiene n.
  - **G3 — Frustración o estándar de la organización.** Si la herramienta externa es el estándar de la organización y si probaron primero algo dentro de Teams. → Segunda mitad de la creencia #1: se van *por* lo que hay dentro o *a pesar* de lo que hay dentro. También anticipa la señal de gasto por fuera de IT, que es la de Lucía.
  - **G4 — Pool de entrevistas.** Recluta Team Leads para `/design-interview` y prioriza a los que dicen que el desvío no les cuesta.
- **Respondentes:** Team Lead de una cuenta de más de 1.000 licencias de Microsoft 365 que convoca o conduce reuniones de 8 o más participantes en Teams. Quedan afuera los que solo asisten (perfil Tomás) y las cuentas chicas.
- **Duración estimada:** 3 preguntas de filtro, 13 preguntas (una condicional) y 3 de opt-in, unos 6 minutos.

## Filtro

S1. ¿Cuántas licencias de Microsoft 365 tiene aproximadamente tu organización? [opción única]
   - Menos de 1.000 → **fin de la encuesta**
   - Entre 1.000 y 5.000
   - Más de 5.000
   - No sé → sigue, marcado como "cuenta no verificada"
   > En el canal dentro de Teams esta pregunta no se muestra: el valor viene de la telemetría como campo oculto.

S2. En las últimas 4 semanas, ¿cuántas reuniones de 8 o más participantes convocaste o condujiste vos? [opción única]
   - Ninguna → **fin de la encuesta**
   - 1 a 3
   - 4 a 8
   - 9 a 15
   - Más de 15

S3. ¿En qué herramienta se hacen la mayoría de esas reuniones? [opción única]
   - Microsoft Teams
   - Zoom → **fin de la encuesta**
   - Google Meet → **fin de la encuesta**
   - Otra → **fin de la encuesta**
   > En el canal dentro de Teams no se muestra.

## Preguntas

*Bloque A. Tu última reunión de 8 o más participantes*

Q1. Pensá en la última reunión de 8 o más participantes que condujiste. ¿Con qué material se trabajó durante la llamada? [opción múltiple]
   - Backlog o tickets (Jira, Azure DevOps, Planner u otro)
   - Tablero visual (Miro, Mural, FigJam, Whiteboard u otro)
   - Documento (Word, Google Docs, Notion, Loop u otro)
   - Dashboard o planilla con datos (Power BI, Excel, Google Sheets u otro)
   - Presentación
   - Ninguno: fue una conversación sin material
   - Otro: ____
   > Objetivo: G1 (tipo de material; separa a Valeria de Gustavo en el análisis)

Q2. En esa reunión, ¿alguien, además de quien compartía pantalla, editó, filtró, votó o anotó sobre ese material durante la llamada? [opción única]
   - Sí, varias personas
   - Sí, una o dos personas
   - No, solo se mostró en pantalla
   - No recuerdo
   > Objetivo: G1 (distingue trabajar en vivo de mostrar; sin esto, el desvío no aplica)

*Bloque B. Las últimas 4 semanas*

Q3. En las últimas 4 semanas, en tus reuniones de 8 o más, ¿cuántas veces pegaste o pediste que se pegara en el chat un enlace para que el grupo entrara a trabajar sobre el material? [opción única]
   - Ninguna → saltar a Q9
   - 1 o 2
   - 3 a 5
   - 6 a 10
   - Más de 10
   > Objetivo: G1 (frecuencia; se cruza con S2 para estimar la proporción de reuniones con desvío)

Q4. ¿A qué herramientas llevaste al grupo esas veces? [opción múltiple]
   - Miro, Mural o FigJam
   - Jira, Azure DevOps u otra herramienta de tickets
   - Google Docs o Google Sheets
   - Notion o Confluence
   - Power BI u otra herramienta de dashboards
   - Word, Excel o PowerPoint en SharePoint u OneDrive
   - Whiteboard o Loop de Microsoft
   - Otra: ____
   > Objetivo: G1 (destino; tablero vs. documento vs. dashboard)

Q5. Pensá en la última vez que pasó. Desde que se pegó el enlace hasta que la mayoría del grupo estaba trabajando sobre el material, ¿cuánto tiempo pasó aproximadamente? [opción única]
   - Menos de 1 minuto
   - Entre 1 y 3 minutos
   - Entre 4 y 6 minutos
   - Entre 7 y 10 minutos
   - Más de 10 minutos
   - No recuerdo
   > Objetivo: G2 (costo en minutos; contrasta los ~5 de Valeria y los ~10 de Gustavo, que son sintéticos)

Q6. En esa misma ocasión, ¿pasó alguna de estas cosas? [opción múltiple]
   - Alguien no tenía acceso o permiso y hubo que pedirlo o darlo
   - Alguien no tenía la licencia de la herramienta
   - Alguien no encontró el enlace en el chat
   - Algunos siguieron mirando solo la pantalla compartida
   - La conversación de la reunión se cortó mientras el grupo trabajaba en la otra herramienta
   - No pasó nada de esto
   - Otra: ____
   > Objetivo: G2 (causas del costo: permisos o licencias, que es la fricción que el mercado documenta, vs. pérdida de ritmo)

Q7. Esa herramienta, ¿cómo llegó a tu equipo? [opción única]
   - Es una herramienta estándar de la organización (la provee IT)
   - La eligió mi equipo o área y IT la aprobó
   - La paga mi equipo o área por fuera de IT (tarjeta corporativa, suscripción propia)
   - Usamos una cuenta gratuita
   - No sé
   > Objetivo: G3 (estándar de la organización vs. elección del equipo; también es señal de gasto por fuera de IT para la creencia de viabilidad)

Q8. Ese día, ¿consideraste hacer ese trabajo dentro de Teams? [opción única]
   - No, en esa reunión siempre se trabaja en esa herramienta
   - No, no sabía que Teams tuviera algo para eso
   - Sí, pero descarté Teams antes de empezar
   - Sí, empezamos en Teams y nos pasamos a la otra herramienta
   > Objetivo: G3 (hábito o estándar vs. descarte o abandono de lo que hay dentro)

*Bloque C. Lo que hay dentro de Teams y lo que queda después*

Q9. En los últimos 3 meses, ¿usaste en una reunión de 8 o más alguna de estas funciones de Teams para trabajar con el grupo? [opción múltiple]
   - Whiteboard
   - Notas de reunión colaborativas o Loop
   - PowerPoint Live o Excel Live
   - Encuestas (Polls/Forms en la reunión)
   - Ninguna
   > Objetivo: G3 (qué se probó; se cruza con Q10)

Q10. *(Solo si eligió alguna función en Q9)* De esas funciones, ¿sigue usándolas tu equipo? [opción única]
   - Sí, en la mayoría de las reuniones en que hace falta
   - A veces
   - Las probamos y las dejamos
   > Objetivo: G3 (adopción vs. abandono; contrasta con el 6% de apertura del Whiteboard y el abandono en menos de 2 minutos)

Q11. Después de tus reuniones de 8 o más, ¿dónde queda lo que se decidió o se trabajó? [opción única]
   - En la herramienta donde se trabajó; no hace falta más
   - Lo paso yo a otro lugar (mail, canal, documento)
   - Lo pasa otra persona del equipo
   - En la grabación o la transcripción
   - No queda registrado en ningún lado
   - Otro: ____
   > Objetivo: G2 (rastro disperso; alimenta también la creencia #7)

Q12. En una semana típica, ¿cuánto tiempo dedicás a pasar en limpio o reconstruir lo que se decidió en esas reuniones? [opción única]
   - Nada
   - Menos de 15 minutos
   - Entre 15 y 30 minutos
   - Entre 30 y 60 minutos
   - Más de 1 hora
   > Objetivo: G2 (costo posterior; contrasta los ~40 min/semana de Valeria, que son sintéticos)

Q13. ¿Qué es lo más difícil de lograr que un grupo de 8 o más personas trabaje sobre el mismo material durante una reunión? [abierta, opcional]
   > Objetivo: G1–G3 (el porqué en sus palabras; se codifica por temas y se lleva a las entrevistas)

Q14. En tu caso, trabajar con el grupo en otra herramienta durante la reunión, fuera de Teams, es… [likert-5, opcional]
   - No es un problema
   - Un problema menor
   - Un problema moderado
   - Un problema serio
   - Un problema muy serio
   > Objetivo: G4 (prioriza en el reclutamiento a quienes dicen que no les cuesta; se contrasta con Q5, Q6 y Q12, que miden comportamiento)

## Filtro para entrevista + opt-in

R1. En esas reuniones, ¿quién decide cómo se trabaja (agenda, formato, herramientas)? [opción única]
   - Yo
   - Lo decidimos entre varios
   - Otra persona; yo solo conduzco → no es candidato
   > Además no son candidatos quienes respondieron "No sé" en S1 o "1 a 3" en S2 (el perfil de entrevista es más estrecho: cuenta verificada y 4 o más reuniones al mes).

R2. ¿Aceptarías una conversación de 30 minutos con nuestro equipo de producto sobre cómo trabajás en estas reuniones? [sí / no]

R3. *(Solo si respondió "sí")* ¿Cómo te contactamos? [abierta, opcional: nombre y mail o usuario de Teams]

## Distribución

| Canal | A quién llega y su sesgo | Alcance aprox. | Link |
|---|---|---|---|
| Encuesta dentro de Teams, al terminar la reunión | Organizadores de reuniones de 8+ en cuentas de 1.000+ licencias, filtrados por telemetría: es el segmento exacto. Es un canal propio, así que sobrerrepresenta a quienes se quedan en Teams y a quienes responden avisos dentro del producto, y subrepresenta a quienes ya trabajan casi todo afuera. Mostrarla a una muestra aleatoria de organizadores, no solo después de reuniones con enlace externo, para no inflar G1. Campos ocultos: tamaño de cuenta y si hubo enlace externo en el chat de esa reunión (telemetría). | unknown: pedir a telemetría cuántos organizadores cumplen el filtro | `{link-teams}` (parámetro `canal=teams`) |
| Comunidad externa de Team Leads ágiles/PM: **nombre a definir antes de publicar** (grupo de LinkedIn o comunidad concreta) | Team Leads que trabajan a diario en Miro, Jira o FigJam: justo los que se van. Sobrerrepresenta equipos de producto y tecnología (perfil Valeria) y subrepresenta la variante Gustavo (operaciones, retail). El tamaño de cuenta es declarado, no verificado (S1). | unknown | `{link-comunidad}` (parámetro `canal=comunidad`) |

- **Meta de n:** ≥100 respondentes que califican con Q1 = backlog, tablero o documento (variante Valeria) y ≥30 con Q1 = dashboard o planilla (variante Gustavo). Por debajo de 30 en cualquiera de los dos, los resultados de ese segmento son direccionales.
- **Viabilidad de la meta:** con los dos alcances en `unknown` no se puede confirmar antes de publicar. Riesgo concreto: la variante Gustavo casi no llega por la comunidad externa, así que depende del canal dentro de Teams. Si en la primera revisión va por debajo de 15, sumar un canal que llegue a operaciones (por ejemplo, Customer Success con cuentas de retail o logística).
- **Primera revisión:** 2026-10-13.
- **Cierre:** abierta hasta llegar a la meta; a más tardar el 2026-10-30, para cumplir con "principios de noviembre" de la agenda.
