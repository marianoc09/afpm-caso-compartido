---
source: survey
survey: product/surveys/2026-09-23-1944-colaboracion-en-vivo-fuera-de-teams.md
results: product/surveys/2026-09-26-1800-respuestas-colaboracion-en-vivo-fuera-de-teams.csv
n: 210 completas (email 76, panel 134) de 249 inicios
opportunity: trabajo-en-vivo-fuera-de-teams
date: 2026-09-29
---

# Análisis de encuesta: trabajo colaborativo fuera de Teams en reuniones de más de 5 participantes

## 1. Denominador y límites

- **Diseño:** `product/surveys/2026-09-23-1944-colaboracion-en-vivo-fuera-de-teams.md` (versión publicada; la del 22/09 es un borrador anterior con otro cuestionario).
- **Ventana real:** 23/09 12:39 → 25/09 09:39. Mediana de 3,5 minutos por respuesta completa.
- **n:** 249 inicios · 34 descalificadas (11 no condujeron reunión de >5, 7 no son empleados, 8 fuera de sector/países en el panel) · 5 parciales · **210 completas** (email 76, panel 134).
- **Tasa de respuesta:** panel 134/150 de cuota (89%). Email: el alcance nunca se confirmó (`unknown` en el diseño), así que no hay tasa; quedó en 76, la mitad de las 150 que el diseño pedía.
- **Metas del diseño:** ≥150 que salen de Teams → **182 ✓** · ≥30 por canal → **✓** · ≥30 que *no* salen → **28 ✗**: todo lo del grupo "En ninguna" es direccional. Las reuniones con externos son 39: también direccional.
- **Sesgo:** dos canales autoseleccionados, uno propio (email: sobrerrepresenta a quienes siguen en Teams y abren mails de Microsoft) y uno pago (panel: firmografía autodeclarada, panelistas motivados por incentivo). **El panel reporta más intensidad de salida** (39% "más de la mitad / todas" vs 21% en email; el email concentra "menos de la mitad": 39% vs 18%). Es un hallazgo sobre la muestra antes que sobre el segmento. Ningún otro corte difiere fuerte entre canales, así que el resto se reporta junto.
- **Consecuencia:** nada de esto alcanza para *confirmar* una creencia; lo máximo es *prometedor* o *debilitado*.

## 2. O1 — Origen del artefacto

**Creíamos:** el tablero o documento externo se crea para colaborar en vivo en la reunión.

**Datos (n=182 que salieron):**

| Q4. Ese tablero o documento... | n | % |
|---|---|---|
| Ya existía antes y se siguió usando después | 92 | 51% |
| Ya existía antes y no se volvió a usar | 5 | 3% |
| Se creó para esa reunión y se siguió usando | 44 | 24% |
| Se creó para esa reunión y no se volvió a usar | 28 | 15% |
| No lo sé | 13 | 7% |

Por herramienta (Q2 × Q4): Jira 73% preexistente · Confluence 77% · dashboards 77% · Notion 52% · Google Docs/Sheets 46% · **Miro 86% creado para la reunión** (55% siguió usándose, 31% se descartó).

Herramientas (Q2, múltiple): Google Docs/Sheets/Slides 32% · Jira u otro gestor 29% · Miro 20% · dashboard 16% · Confluence 14% · Notion 12% · FigJam 12% · Slido/Mentimeter 9% · Mural 9% · Otra 5% (Canva, ClickUp, Excel en SharePoint, Retrotool, Trello) · Lucidspark 4%. Email más Jira (35%); panel más Google Docs (36%) y dashboards (21% vs 8%).

Cómo llegaron (Q3): enlace en el chat **54%** · **ya la tenían abierta 22%** · pantalla compartida y cada uno la abre 15% · app dentro de la reunión de Teams 8% · otro 1%. → **46% de los desvíos no dejan enlace en el chat**: la telemetría del 29% de reuniones con enlace externo subestima el fenómeno.

**Decisión:** el problema se parte en dos. Para backlog, wiki y datos (más de la mitad de los casos) es *integración con el sistema donde ya vive el trabajo*; solo la variante tablero (Miro/FigJam/Mural, ~1 de cada 3) es *colaboración en vivo* pura. Una solución que solo compita con Miro deja afuera la mayoría de los casos.

## 3. O2 — Costo de acceso

**Creíamos:** ~5 minutos por reunión hasta que todos entran; gente que queda afuera.

**Datos (n=182):**

| Q6. Tiempo hasta que todos estuvieron dentro | Todos | Reuniones internas (n=137) | Con externos (n=39, direccional) |
|---|---|---|---|
| Menos de 1 minuto | 19% | 25% | 3% |
| Entre 1 y 2 minutos | 27% | 32% | 10% |
| Entre 3 y 4 minutos | 20% | 18% | 21% |
| Entre 5 y 9 minutos | 21% | 13% | **51%** |
| 10 minutos o más | 6% | 4% | 10% |
| No lo sé | 7% | 7% | 5% |
| **≥5 minutos** | **27%** | **18%** | **62%** |

Q7, alguien quedó afuera mirando la pantalla de otro: **51%** de los casos (1 persona 27%, 2–3 18%, 4+ 5%, no sabe 3%). Internas 46%, con externos 64%.

Q8, externos en la reunión: no 75% · sí, 1 → 9% · sí, 2 o más → 12% · no sabe 3%.

**Decisión:** el umbral de 5 minutos **no se sostiene como costo típico** del Team Lead en reuniones internas (18%); la fricción de acceso se concentra en reuniones con clientes o agencias (permisos, SSO, licencias por filial: R-141, R-183, R-205, R-244). Eso es otro segmento u otro problema (acceso de invitados), no el núcleo de la oportunidad. Lo transversal es que **la mitad de las veces alguien queda mirando**, aun sin externos: el costo no es de minutos sino de participación.

## 4. O3 — Qué se hace afuera y dónde queda la decisión

**Actividades (Q5, múltiple, n=182):** votar o priorizar **40%** · editar un documento entre varios 35% · revisar datos o métricas y señalar algo 34% · anotar decisiones o acuerdos 33% · aportar ideas 29% · actualizar tareas o tickets 25% · agrupar u ordenar ideas 22% · dibujar un diagrama 13% · otro 5% (planning poker, revisar incidentes, presupuesto, roadmap). No es "pizarra": la actividad #1 es **decidir**, y hay un bloque de datos del 34%.

**Dónde queda la decisión (Q9, múltiple, n=182):** **no quedó registrada 24%** · chat fuera de Teams (Slack/WhatsApp) 23% · Jira 23% · **otro 18%** · misma herramienta externa 15% · chat o notas de la reunión de Teams 13% · documento de actas 12% · correo 10% · no se tomaron decisiones 7%. Email deja más en Teams (23% vs 7% en panel); panel más en Slack/WhatsApp (26% vs 18%).

El 18% de "Otro" supera el 15% que el diseño fijó como alarma: la lista estaba incompleta. Lo que falta es **"el resumen de IA / recap de Copilot"** (≈20 de 32 "Otro"), casi siempre con un pero: "resume todo pero no distingue lo decidido", "le faltaba quién hacía qué", "lo tuve que corregir", "que nadie leyó". El resto: grabación o transcripción (6), OneNote, cuaderno, nota de voz por WhatsApp, comentario en el documento.

**Abierta Q11, "lo más difícil de lograr que el grupo trabaje junto y llegue a una decisión" (n=95), codificada:**

| Tema | Menciones | Verbatim |
|---|---|---|
| Registro y continuidad entre reuniones: dónde quedó, quién hace qué, retomar la próxima vez, que no se reabra | 31 | "Cada reunión es una isla. Lo que se trabajó en la anterior está en otro lado" (R-166) · "Que quede registro del POR QUÉ decidimos algo. El qué queda en Jira, el por qué se pierde" (R-207) · "Tuvimos un release que salió con el alcance viejo porque la decisión quedó en un comentario" (R-144) |
| Converger y decidir: votar, cerrar, consenso, que alguien decida | 14 | "Divergir es fácil, todos tiran ideas. Ordenarlas y elegir es lo que nos cuesta" (R-011) · "Usamos reacciones en el chat pero nadie sabe cuántos votaron ni qué ganó" (R-053) |
| Participación y atención: cámaras apagadas, los mismos de siempre, celular, gente que no sabe usar la herramienta | 11 | "Hay 12 personas y opinan 3, el resto escucha o está en otra cosa" (R-049) · "Algunos no saben usar Miro y se quedan mirando. Pierdo gente en el camino" (R-147) |
| Logística: husos horarios, demasiadas reuniones, audio, rendimiento de Teams | 11 | "Coordinar horarios entre 4 países" (R-075) |
| Whiteboard nativo insuficiente o escondido: sin votar ni agrupar, sin plantillas, se pierde a la semana, lento con 8+ | 10 | "Armé una retro en la whiteboard de Teams y a la semana siguiente no la pude encontrar para continuar. Volvimos a Miro" (R-089) · "El whiteboard no deja ordenar ni votar, es una hoja en blanco y ya" (R-239) |
| Acceso a la herramienta externa: externos, permisos, SSO, licencias por filial | 10 | "Los permisos del Miro. Siempre hay alguien que no puede editar y pierde los primeros 10 minutos" (R-244) · "Cuando vienen externos es un desastre, que no tienen acceso, que les pide cuenta, que el link no abre" (R-141) |
| Compliance o normativa prohíbe herramientas externas | 3 (+2 en Q12) | "Compliance no nos deja meter datos de clientes en Miro, así que o lo hacemos en Teams o no se hace. Y en Teams cuesta" (R-190) · "Con la normativa europea tenemos las herramientas externas muy limitadas. Lo que hay dentro de Teams tendría que funcionar mejor" (R-173) |
| Todos mirando el mismo dato | 1 (+2 en Q12) | "Cada uno abre el dashboard con su filtro y estamos hablando de números distintos" (R-036) |
| Sin problema | 3 | "No hay problema real, funcionamos bien" (R-181) |

**Decisión:** el dolor dominante en palabras propias **no es la entrada a la herramienta sino la salida: qué quedó decidido, quién lo hace y cómo se retoma la próxima vez**. Eso reencuadra la oportunidad hacia "decidir y dejar rastro" (cruza con la creencia #7) y le da un lugar concreto a la IA: separar decisiones de conversación y asignarles dueño, que es justo lo que quienes usan el recap dicen que falla.

## 5. O4 — Conocimiento y uso de lo nativo (n=210)

| Función | No sabía que existía | Sé que existe, nunca la usé | La usé y dejé de usarla | La uso en algunas | La uso en la mayoría |
|---|---|---|---|---|---|
| Whiteboard | 8% | 27% | **43%** | 17% | 4% |
| Notas de la reunión (Loop) | **31%** | 28% | 14% | 20% | 8% |
| Apps de terceros dentro de la reunión | **40%** | 28% | 9% | 18% | 5% |
| Resumen o asistente de IA | 12% | 39% | 13% | 22% | 14% |

Por canal: el email conoce más Copilot (solo 5% no sabía vs 16% en panel) y usa un poco más las notas (37% vs 22%); en el resto, las proporciones son parecidas.

**Decisión:** son dos problemas distintos. **Whiteboard es "no me sirve"**: la probaron y la abandonaron (43%), con motivos concretos en Q11 (no vota, no agrupa, sin plantillas, se pierde a la semana, lento con 8+). **Notas y apps embebidas son "no sé que existe"** (31% y 40%): la función que resolvería el 8% de "app dentro de Teams" (Q3) es invisible para 4 de cada 10. Copilot es lo más adoptado (36%) y lo que más quejas de calidad concentra.

## 6. Los que no salen (Q1 = "En ninguna", n=28, direccional)

Q12, cómo aportan, priorizan o deciden (n=16): hablando y alguien anota (6) · levantan la mano o reacciones en el chat (4) · pantalla compartida de Excel donde el líder escribe (2: "es un lío saber a qué fila se refieren") · propuesta por mail antes (1) · notas de la reunión de Teams (1) · Whiteboard "cuando no queda otra" o "se traba" (2) · **compliance les prohíbe salir** (2) · las decisiones se toman en reuniones más chicas (1). No contradicen la creencia por estar conformes con lo nativo: la mayoría hace lo mismo con menos herramienta.

## 7. Región (D1, n=210)

México 22% · Colombia 20% · Argentina 15% · España 13% · Estados Unidos 11% · Chile 9% · Perú 6% · otros 6% (Brasil, Uruguay, Costa Rica, Ecuador). España (27) es la muestra con operación en el EEE; dos de las cinco menciones de compliance son de ahí.

## 8. Insights priorizados

1. **La mayor parte del "desvío" es integración, no colaboración en vivo.** 53% de los artefactos preexisten y siguen viviendo afuera; 46% de los desvíos no dejan enlace en el chat. Reencuadra el alcance y corrige la lectura de la telemetría.
2. **El costo de entrada de 5 minutos está en las reuniones con externos, no en las internas** (62% vs 18%). El Team Lead interno pierde poco tiempo entrando; pierde después.
3. **El rastro es el dolor #1.** 24% de las decisiones no queda registrada, 23% queda en Slack/WhatsApp, y el recap de IA que ~20 respondentes usan como registro no distingue decisiones ni dueños. 31 de 95 abiertas. La actividad #1 afuera es votar/priorizar.
4. **Whiteboard fue probado y abandonado por el 43%.** Lo que reemplace a Miro no puede ser una hoja en blanco: votar, agrupar, plantillas y un enlace fijo que sobreviva a la reunión.
5. **Notas y apps embebidas tienen un problema de descubrimiento antes que de producto** (31–40% no sabe que existen).
6. **Señal para viabilidad (creencia #3):** compliance o normativa europea aparece 5 veces sin preguntarlo, como razón para quedarse dentro de Teams y sufrirlo.

## 9. Porqués abiertos (candidatos para entrevistas)

- Por qué el tablero de Miro se crea para la reunión y en un tercio de los casos no se retoma: ¿es descartable por diseño o se pierde?
- Qué hace el Team Lead con la mitad que quedó mirando: ¿la da por perdida, la incorpora por voz, cambia de herramienta?
- Por qué el recap de IA no alcanza como registro: ¿formato, confianza, dónde vive, quién lo lee?
- Cómo deciden hoy los que votan con reacciones del chat, y qué pasa cuando "termino decidiendo yo".
- Qué haría el 40% que no conoce las apps embebidas si las conociera: ¿resuelve el desvío o lo reproduce adentro?
- Para la variante datos (34% revisa métricas): qué significa "todos mirando el mismo número" y cuánto pesa el dashboard preexistente.

## 10. Notas de método

- La opción "resumen de IA / recap de Copilot" falta en Q9; el 18% de "Otro" lo explica. Agregarla si la encuesta se repite (registrado en `product/corrections.md`).
- El corte interno/externo (Q8) se toma como definitorio con n=39 externos: es direccional y debería confirmarse en entrevistas antes de descartar el segmento.
- La diferencia de intensidad entre canales (Q1) no se puede atribuir al segmento: puede ser sesgo del panel (incentivo) o del email (conformes con Teams).
- Los contactos del pool son los que dejó el formulario (dominio de ejemplo en este export).

## 11. Pool de reclutamiento para entrevistas

Criterio: R1 = No (no administra M365), R2 ≥ "2 o 3" reuniones por semana, R3 = Sí. **64 candidatos** (panel 48, email 16). Etiquetas de contradicción según el diseño: Q1 "En ninguna", Q4 "Ya existía…", Q6 ≤ 2 minutos. **47 contradicen** al menos un supuesto, 17 confirman. Orden sugerido: primero los que no salen (con preferencia por R-143, R-153, R-009 por compliance y uso de recap, y por los de 4+ reuniones/semana), después los que salen a un artefacto preexistente y entran en menos de 2 minutos (R-224, R-234, R-229, R-128, R-131, R-144…), y al final los que confirman (R-113, R-024, R-097, R-099, R-101, R-205).

| ID | Canal | País | Reuniones/sem | Etiqueta | Respuestas clave | Contacto |
|---|---|---|---|---|---|---|
| R-009 | email | Colombia | 2 o 3 | no sale | En ninguna | Jimena Paz, jimena.paz@example.com |
| R-046 | email | Argentina | 2 o 3 | no sale | En ninguna | Mateo Gómez, mateo.gomez@example.com |
| R-085 | panel | Colombia | 4 o más | no sale | En ninguna | Isabella Vargas, isabella.vargas@example.com |
| R-088 | panel | Argentina | 2 o 3 | no sale | En ninguna | Ana Lozano, ana.lozano@example.com |
| R-110 | panel | España | 2 o 3 | no sale | En ninguna |  |
| R-120 | panel | Colombia | 2 o 3 | no sale | En ninguna | irene.blanco@example.com |
| R-135 | email | Otro: Brasil | 2 o 3 | no sale | En ninguna | Álvaro Cano, alvaro.cano@example.com |
| R-143 | email | España | 4 o más | no sale | En ninguna | Lucía Fernández, lucia.fernandez@example.com |
| R-153 | email | Argentina | 4 o más | no sale | En ninguna | Paula paula.benitez@example.com |
| R-170 | panel | Colombia | 2 o 3 | no sale | En ninguna | Andrés Quintero, andres.quintero@example.com |
| R-196 | panel | México | 4 o más | no sale | En ninguna | Ricardo Salinas, ricardo.salinas@example.com |
| R-242 | panel | México | 4 o más | no sale | En ninguna | Rocío Figueroa, rocio.figueroa@example.com |
| R-013 | email | México | 2 o 3 | entra en ≤2 min | En menos de la mitad · Se creó y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Víctor Durán, victor.duran@example.com |
| R-036 | email | Perú | 2 o 3 | artefacto preexistente; entra en ≤2 min | En aproximadamente la mitad · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Diego Paredes, diego.paredes@example.com |
| R-042 | email | Colombia | 2 o 3 | artefacto preexistente | En menos de la mitad · Ya existía y se siguió usando después · Entre 5 y 9 minutos · afuera: 1 · externos: Sí, 1 | Silvia Montes, silvia.montes@example.com |
| R-057 | panel | México | 2 o 3 | artefacto preexistente; entra en ≤2 min | En todas · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | florencia.medina@example.com |
| R-065 | panel | Estados Unidos | 2 o 3 | artefacto preexistente | En aproximadamente la mitad · Ya existía y se siguió usando después · Entre 3 y 4 minutos · afuera: 1 · externos: No | carla.munoz@example.com |
| R-074 | panel | España | 2 o 3 | entra en ≤2 min | En aproximadamente la mitad · No lo sé · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Braulio braulio.aranda@example.com |
| R-086 | panel | México | 2 o 3 | artefacto preexistente | En más de la mitad · Ya existía y se siguió usando después · Entre 3 y 4 minutos · afuera: Ninguno · externos: No lo sé | Laura Gil, laura.gil@example.com |
| R-089 | panel | Colombia | 2 o 3 | entra en ≤2 min | En aproximadamente la mitad · Se creó y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Ximena Aguilar, ximena.aguilar@example.com |
| R-090 | panel | España | 4 o más | entra en ≤2 min | En menos de la mitad · Se creó y se siguió usando después · Menos de 1 minuto · afuera: Ninguno · externos: No | Luis Carrasco, luis.carrasco@example.com |
| R-093 | panel | Argentina | 2 o 3 | entra en ≤2 min | En más de la mitad · Se creó y se siguió usando después · Entre 1 y 2 minutos · afuera: 1 · externos: No | mauricio.pineda@example.com |
| R-094 | panel | Estados Unidos | 2 o 3 | artefacto preexistente; entra en ≤2 min | En aproximadamente la mitad · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | alejandro.navarro@example.com |
| R-102 | panel | Colombia | 2 o 3 | artefacto preexistente; entra en ≤2 min | En más de la mitad · Ya existía y no se volvió a usar · Entre 1 y 2 minutos · afuera: 1 · externos: No | Nicolás Castillo, nicolas.castillo@example.com |
| R-128 | panel | Argentina | 2 o 3 | artefacto preexistente; entra en ≤2 min | En todas · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Ignacio Arce, ignacio.arce@example.com |
| R-131 | email | España | 2 o 3 | artefacto preexistente; entra en ≤2 min | En aproximadamente la mitad · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Sara Molina, sara.molina@example.com |
| R-132 | panel | Argentina | 4 o más | artefacto preexistente | En más de la mitad · Ya existía y se siguió usando después · Entre 3 y 4 minutos · afuera: 1 · externos: No |  |
| R-144 | panel | Chile | 2 o 3 | artefacto preexistente; entra en ≤2 min | En aproximadamente la mitad · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Pilar Ruiz, pilar.ruiz@example.com |
| R-151 | panel | México | 2 o 3 | artefacto preexistente; entra en ≤2 min | En más de la mitad · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: 1 · externos: No | sofia.martinez@example.com |
| R-159 | panel | Colombia | 4 o más | artefacto preexistente | En todas · Ya existía y se siguió usando después · Entre 3 y 4 minutos · afuera: 4 o más · externos: No lo sé | natalia.suarez@example.com |
| R-171 | panel | Colombia | 2 o 3 | artefacto preexistente | En menos de la mitad · Ya existía y se siguió usando después · Entre 3 y 4 minutos · afuera: Ninguno · externos: No | hugo.arriaga@example.com |
| R-173 | panel | España | 2 o 3 | entra en ≤2 min | En más de la mitad · Se creó y no se volvió a usar · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Josefina Palma, josefina.palma@example.com |
| R-176 | panel | Argentina | 2 o 3 | artefacto preexistente; entra en ≤2 min | En aproximadamente la mitad · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Emiliano Cabrera, emiliano.cabrera@example.com |
| R-180 | email | Argentina | 2 o 3 | artefacto preexistente; entra en ≤2 min | En menos de la mitad · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Agustín Ledesma, agustin.ledesma@example.com |
| R-194 | panel | Chile | 2 o 3 | artefacto preexistente; entra en ≤2 min | En todas · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: 1 · externos: No |  |
| R-201 | panel | Estados Unidos | 2 o 3 | artefacto preexistente | En más de la mitad · Ya existía y se siguió usando después · Entre 3 y 4 minutos · afuera: Ninguno · externos: No | Gabriela Mendoza, gabriela.mendoza@example.com |
| R-224 | panel | Chile | 4 o más | artefacto preexistente; entra en ≤2 min | En más de la mitad · Ya existía y se siguió usando después · Menos de 1 minuto · afuera: Ninguno · externos: No | Martina Rojas, martina.rojas@example.com |
| R-227 | panel | Argentina | 2 o 3 | artefacto preexistente | En aproximadamente la mitad · Ya existía y se siguió usando después · Entre 5 y 9 minutos · afuera: Ninguno · externos: Sí, 2 o más |  |
| R-228 | panel | Estados Unidos | 2 o 3 | artefacto preexistente | En más de la mitad · Ya existía y se siguió usando después · Entre 5 y 9 minutos · afuera: 2 o 3 · externos: Sí, 2 o más | Pablo Domínguez, pablo.dominguez@example.com |
| R-229 | panel | Colombia | 4 o más | artefacto preexistente; entra en ≤2 min | En aproximadamente la mitad · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Tatiana Rincón, tatiana.rincon@example.com |
| R-230 | panel | Perú | 2 o 3 | entra en ≤2 min | En aproximadamente la mitad · Se creó y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Elena Prieto, elena.prieto@example.com |
| R-234 | panel | Chile | 4 o más | artefacto preexistente; entra en ≤2 min | En menos de la mitad · Ya existía y se siguió usando después · Menos de 1 minuto · afuera: Ninguno · externos: No | martin.espinoza@example.com |
| R-235 | panel | Colombia | 2 o 3 | artefacto preexistente; entra en ≤2 min | En todas · Ya existía y se siguió usando después · Entre 1 y 2 minutos · afuera: Ninguno · externos: No | Felipe felipe.acosta@example.com |
| R-238 | panel | Estados Unidos | 4 o más | artefacto preexistente | En más de la mitad · Ya existía y se siguió usando después · Entre 3 y 4 minutos · afuera: 1 · externos: No | Micaela Correa, micaela.correa@example.com |
| R-240 | panel | Estados Unidos | 2 o 3 | artefacto preexistente; entra en ≤2 min | En aproximadamente la mitad · Ya existía y se siguió usando después · Menos de 1 minuto · afuera: 1 · externos: No | Constanza Lagos, constanza.lagos@example.com |
| R-244 | panel | Perú | 2 o 3 | artefacto preexistente | En aproximadamente la mitad · Ya existía y se siguió usando después · Entre 5 y 9 minutos · afuera: 2 o 3 · externos: Sí, 2 o más | Gonzalo Reyes, gonzalo.reyes@example.com |
| R-247 | panel | México | 2 o 3 | artefacto preexistente; entra en ≤2 min | En aproximadamente la mitad · Ya existía y se siguió usando después · Menos de 1 minuto · afuera: Ninguno · externos: No | marcos.silva@example.com |
| R-006 | email | Estados Unidos | 4 o más | confirma | En menos de la mitad · No lo sé · Entre 3 y 4 minutos · afuera: 2 o 3 · externos: No | Cristian cristian.maldonado@example.com |
| R-011 | email | España | 2 o 3 | confirma | En aproximadamente la mitad · Se creó y se siguió usando después · No lo sé · afuera: 4 o más · externos: No | Valentina Herrera, valentina.herrera@example.com |
| R-019 | email | Colombia | 2 o 3 | confirma | En aproximadamente la mitad · Se creó y se siguió usando después · Entre 3 y 4 minutos · afuera: Ninguno · externos: No | Brenda Solís, brenda.solis@example.com |
| R-024 | email | Colombia | 2 o 3 | confirma | En menos de la mitad · Se creó y no se volvió a usar · Entre 5 y 9 minutos · afuera: 1 · externos: No | valeria.castro@example.com |
| R-031 | email | México | 4 o más | confirma | En aproximadamente la mitad · Se creó y se siguió usando después · Entre 5 y 9 minutos · afuera: Ninguno · externos: Sí, 2 o más | Verónica veronica.fuentes@example.com |
| R-038 | email | México | 2 o 3 | confirma | En aproximadamente la mitad · Se creó y no se volvió a usar · Entre 3 y 4 minutos · afuera: 1 · externos: No | Emilio Soto, emilio.soto@example.com |
| R-070 | panel | Colombia | 2 o 3 | confirma | En aproximadamente la mitad · No lo sé · No lo sé · afuera: 2 o 3 · externos: No | Clara Iglesias, clara.iglesias@example.com |
| R-076 | panel | Chile | 4 o más | confirma | En menos de la mitad · Se creó y no se volvió a usar · No lo sé · afuera: 2 o 3 · externos: Sí, 1 |  |
| R-077 | panel | México | 4 o más | confirma | En menos de la mitad · Se creó y se siguió usando después · Entre 5 y 9 minutos · afuera: No lo sé · externos: Sí, 1 | Beatriz Serrano, beatriz.serrano@example.com |
| R-097 | panel | España | 4 o más | confirma | En más de la mitad · Se creó y se siguió usando después · 10 minutos o más · afuera: 2 o 3 · externos: No | Javier javier.molina@example.com |
| R-099 | panel | Colombia | 2 o 3 | confirma | En aproximadamente la mitad · Se creó y no se volvió a usar · 10 minutos o más · afuera: 1 · externos: Sí, 2 o más | Santiago Ríos, santiago.rios@example.com |
| R-101 | panel | España | 2 o 3 | confirma | En más de la mitad · Se creó y se siguió usando después · Entre 5 y 9 minutos · afuera: 2 o 3 · externos: No | Hernán hernan.vidal@example.com |
| R-103 | panel | México | 2 o 3 | confirma | En aproximadamente la mitad · Se creó y se siguió usando después · Entre 5 y 9 minutos · afuera: 1 · externos: No lo sé | ivan.cordero@example.com |
| R-113 | panel | Argentina | 4 o más | confirma | En todas · Se creó y se siguió usando después · Entre 5 y 9 minutos · afuera: 2 o 3 · externos: No | Tomás Aguirre, tomas.aguirre@example.com |
| R-204 | panel | Colombia | 2 o 3 | confirma | En todas · Se creó y no se volvió a usar · Entre 3 y 4 minutos · afuera: Ninguno · externos: Sí, 1 | noelia.ferrer@example.com |
| R-205 | panel | Argentina | 2 o 3 | confirma | En menos de la mitad · Se creó y se siguió usando después · Entre 5 y 9 minutos · afuera: 4 o más · externos: Sí, 2 o más | fernando.quiroga@example.com |
| R-245 | panel | México | 4 o más | confirma | En aproximadamente la mitad · Se creó y no se volvió a usar · Entre 5 y 9 minutos · afuera: 2 o 3 · externos: No |  |
