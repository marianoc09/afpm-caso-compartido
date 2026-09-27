# Skill reference — plugin `afpm` (AI-First Product Manager)

Referencia rápida de las skills del plugin `afpm` (Alaimo Labs) usadas en el caso compartido de AFPM. Todos los artefactos son markdown dentro de `product/` en el repo; ningún servicio externo. El contenido de las skills está en inglés, pero los entregables salen en el idioma en que se trabaja.

## Flujo recomendado (Opportunity Solution Tree)

```
/start-product  →  product/overview.md   (contexto + registro único de creencias)
      ↓
/frame-opportunity  →  product/opportunities/   (problema + segmento + señales, sin solución)
      ↓
/clarify-idea  →  product/ideas/   (solución candidata, colgada de una oportunidad)
      ↓
/write-spec  →  product/specs/   (journey, stories, criterios, hipótesis falsable)
      ↓
/slice-feature  →  product/exposure-plans/   (niveles de reveal, cada uno prueba una creencia)
```

Alrededor de ese tronco, las skills de research (personas, entrevistas, encuestas, secondary research, fricciones) alimentan `product/insights/` y actualizan el estado de las creencias en `overview.md`. Saltear el nivel de oportunidad está permitido, pero es una decisión declarada: el idea brief registra `opportunity: none (declared)` y el problema asumido se registra como creencia.

## Workflows skills (slash commands — se invocan a mano, nunca se cargan solos)

| Comando                 | Qué hace                                                                                                                                                                                                                   | Argumento                                                                                  | Lee de                                       | Escribe en                                           |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------------- | ---------------------------------------------------- |
| `/start-product`        | Ubica el producto en dos ejes (nuevo/existente, comercial/interno), captura contexto, sponsor (si es interno) y una lista rankeada y tagueada de creencias no verificadas. Es el contexto que leen todas las demás skills. | `[nombre o idea en una línea; vacío para ser entrevistado]`                                | —                                            | `product/overview.md`                                |
| `/frame-opportunity`    | Enmarca una oportunidad: un problema para un segmento, respaldado por señales, antes de elegir solución. Pregunta de a una; lo desconocido se vuelve creencia. La salida es una agenda de research, no una feature.        | `<la oportunidad como llegó: línea de estrategia, señal, pedido o idea>`                   | `overview.md`, `personas/`, `insights/`      | `product/opportunities/{fecha}-{slug}.md`            |
| `/research-market`      | Secondary research / benchmarking (competidores, alternativas, precios, tendencias). Cada afirmación lleva etiqueta de procedencia y se mapea a las creencias del overview.                                                | `[pregunta, tema o archivo de oportunidad; por defecto deriva preguntas de las creencias]` | `overview.md`, `opportunities/`, `insights/` | `product/research/{fecha}-{slug}.md`                 |
| `/generate-personas`    | Genera un set diverso de personas sintéticas, listas para entrevistas y críticas.                                                                                                                                          | `[cantidad y/o foco, ej. "3 personas para el segmento B2B"]`                               | `overview.md`                                | `product/personas/{nombre-slug}.md`                  |
| `/interview-persona`    | Entrevista a una persona sintética. Modo **exploration** (descubrimiento abierto de dolores y workflows) o **validation** (feedback estructurado sobre una idea).                                                          | `<persona> [exploration\|validation] [tema]`                                               | `personas/`                                  | `product/interviews/{fecha}-{persona-slug}.md`       |
| `/extract-insights`     | Extrae insights accionables de una o más transcripciones (sintéticas o reales). Propone anotaciones de estado sobre creencias; vos aprobás.                                                                                | `[transcripciones o persona; por defecto la última entrevista]`                            | `interviews/`                                | `product/insights/{fecha}-{slug}.md`                 |
| `/design-interview`     | Diseña una guía de entrevista + plan de reclutamiento (primero los opt-ins de encuestas) para research con usuarios reales, anclada en insights, supuestos y personas.                                                     | `[qué querés aprender/validar, o un archivo de oportunidad/insight/idea/spec]`             | `insights/`, `opportunities/`, `research/`   | `product/interview-guides/{fecha}-{slug}.md`         |
| `/test-interview-guide` | Pretestea una guía corriéndola contra una persona sintética: detecta preguntas sugestivas, callejones sin salida y huecos de cobertura, y la revisa.                                                                       | `[guía; por defecto la más reciente] [persona; por defecto el perfil de la guía]`          | `interview-guides/`, `personas/`             | `product/interviews/{fecha}-pretest-{guide-slug}.md` |
| `/design-survey`        | Diseña un cuestionario con bloque de opt-in a entrevista, listo para pegar en cualquier herramienta de encuestas.                                                                                                          | `[qué medir/validar, o un archivo de oportunidad/insight/idea/spec]`                       | `opportunities/`, `research/`, `insights/`   | `product/surveys/{fecha}-{slug}.md`                  |
| `/analyze-survey`       | Analiza resultados: resumen cuantitativo por objetivo de aprendizaje, codificación de abiertas, insights. Propone anotaciones de estado sobre creencias.                                                                   | `[archivo de resultados CSV/markdown o datos pegados; opcional el diseño de la encuesta]`  | `surveys/`                                   | `product/insights/{fecha}-{slug}.md`                 |
| `/derive-personas`      | Deriva personas basadas en evidencia a partir de patrones que se repiten en entrevistas y encuestas reales. Cada rasgo es trazable a evidencia.                                                                            | `[archivos de entrevistas/encuestas; por defecto todo el material real en product/]`       | `interviews/`, `insights/`                   | `product/personas/{nombre-slug}.md`                  |
| `/map-frictions`        | Analiza un user journey paso a paso para identificar fricciones cognitivas donde la IA agrega valor real (Mapa de Fricciones Cognitivas).                                                                                  | `[archivo o descripción del journey; lo elicita si no existe]`                             | `personas/`, `specs/`                        | `product/journeys/{fecha}-{journey-slug}.md`         |
| `/clarify-idea`         | Toma una idea difusa y la afila con preguntas de a una, ancladas en evidencia. Nombra su oportunidad padre o declara que no tiene. Las decisiones quedan tuyas; lo desconocido se vuelve supuesto.                         | `<la idea en una o dos oraciones>`                                                         | `opportunities/`, `research/`                | `product/ideas/{fecha}-{slug}.md`                    |
| `/write-spec`           | Redacta una spec anclada en evidencia: problema, user journey, user stories críticas con criterios de aceptación, hipótesis falsable, supuestos tagueados por riesgo.                                                      | `[idea o archivo de insight; por defecto elige entre insights recientes]`                  | `insights/`, `personas/`, `research/`        | `product/specs/{fecha}-{slug}.md`                    |
| `/critique-spec`        | Panel de personas sintéticas critica una spec/PRD/idea: reviews individuales en personaje + síntesis del panel.                                                                                                            | `<spec o idea> [personas; por defecto todas]`                                              | `specs/`, `personas/`                        | `product/insights/{fecha}-critique-{spec-slug}.md`   |
| `/slice-feature`        | Convierte la hipótesis de una spec en un Exposure Plan: niveles acumulativos de reveal, cada uno prueba una creencia falsable.                                                                                             | `<spec> [flags\|incremental]`                                                              | `specs/`                                     | `product/exposure-plans/{fecha}-{spec-slug}.md`      |
| `/review-evidence`      | Barrido semanal: artefactos nuevos vs. creencias del overview, propone anotaciones de estado, reporta qué está derivando y registra correcciones humanas a propuestas de la IA.                                            | `[ventana, ej. "last 2 weeks"; por defecto desde la última revisión]`                      | todo `product/`                              | `overview.md` (estados), `product/corrections.md`    |

## Knowledge skills (se cargan solas cuando el tema coincide)

| Skill                  | Conocimiento que aporta                                                                                                                                           | Cuándo se activa                                                                                                                                   |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `opportunity-framing`  | Oportunidad vs. solución vs. outcome; señales vs. prueba; creencias de valor y viabilidad de una oportunidad; agenda de research; el OST como layout de archivos. | Al enmarcar una oportunidad, decidir si algo es problema o solución, o cuando una idea llega como solución y hay que encontrar el problema debajo. |
| `secondary-research`   | Disciplina de procedencia, jerarquía de fuentes, lanes (competidores, alternativas, precios, tendencias), mapeo a creencias no verificadas.                       | Al investigar un mercado, hacer benchmarking o dimensionar una oportunidad.                                                                        |
| `synthetic-personas`   | Principios de arquetipos, estructura de una persona, requisitos de diversidad.                                                                                    | Al crear personas, arquetipos o modelar segmentos.                                                                                                 |
| `synthetic-interviews` | Roleplay en personaje; modo exploration vs. validation.                                                                                                           | Al entrevistar o simular un usuario.                                                                                                               |
| `insight-extraction`   | Áreas de foco, reglas de anclaje, barra de calidad de un insight.                                                                                                 | Al sintetizar entrevistas o feedback en decisiones de producto.                                                                                    |
| `interview-guides`     | De objetivos de aprendizaje a preguntas abiertas no sugestivas; estructura de embudo; probes; pretesting.                                                         | Al diseñar una guía de entrevista para usuarios reales.                                                                                            |
| `survey-design`        | Tipos de pregunta, sesgo de redacción, orden, escalas; resumen cuantitativo y codificación de abiertas.                                                           | Al diseñar o analizar una encuesta.                                                                                                                |
| `cognitive-frictions`  | El lente MFC: cuatro categorías de fricción (transformación, limitador, estandarizador, evaluador), severidad, barra de oportunidad.                              | Al buscar dónde la IA agrega valor en un journey.                                                                                                  |
| `feature-specs`        | Estructura de spec: journey, stories, criterios, hipótesis, supuestos tagueados por riesgo.                                                                       | Al escribir una spec o PRD, stories o criterios de aceptación.                                                                                     |
| `persona-critique`     | Reviews en personaje y síntesis de panel con rating estructurado.                                                                                                 | Al criticar una spec con personas o correr un panel.                                                                                               |
| `exposure-plans`       | Build ≠ reveal, descomposición de creencias, diseño de niveles, validaciones.                                                                                     | Al rebanar una feature o planear un reveal progresivo.                                                                                             |

## Convenciones de archivos

```
product/
├── overview.md          # contexto, sponsor (interno), registro único de creencias tagueadas y rankeadas
├── corrections.md       # log de correcciones humanas a propuestas de la IA (lo mantiene /review-evidence)
├── personas/            # una por archivo (sintética o derivada)
├── interviews/          # transcripciones, sintéticas y reales
├── interview-guides/    # guías para entrevistas reales
├── surveys/             # cuestionarios
├── insights/            # insights, análisis de encuestas y paneles de crítica
├── research/            # secondary research y benchmarks
├── journeys/            # user journeys + mapas de fricción cognitiva
├── opportunities/       # briefs de oportunidad: problema + segmento + señales + agenda, sin solución
├── ideas/               # ideas clarificadas (cada una nombra su oportunidad padre o `none (declared)`)
├── specs/               # specs de features
└── exposure-plans/      # exposure plans
```

Los archivos fechados usan el prefijo `{YYYY-MM-DD-HHMM}-{slug}.md`.

## Reglas del registro de creencias (`overview.md`)

- Es el **único** registro: ninguna creencia vive en listas por oportunidad, idea o spec.
- Cada creencia lleva tag de **alcance** — `[product]`, `[opportunity: {slug}]`, `[feature: {slug}]` — y de **riesgo** — `[value]`, `[usability]`, `[feasibility]`, `[viability]` — y se rankea por impacto × incertidumbre.
- Valor se responde con usuarios (entrevistas, observación, uso); viabilidad se responde con el negocio (ingresos, disposición a pagar o, en producto interno, el sponsor y su métrica).
- Producto interno: se registra el **sponsor** (quién financia y qué necesita ver para seguir financiando).
- A medida que llega evidencia, el estado se anota en la misma línea de la creencia: `— confirmed/contradicted/weakened by [archivo] (fecha)`. Sin estado = sigue sin verificar. Las keywords quedan en inglés.
- Solo la evidencia de **usuarios reales** confirma; la evidencia sintética solo vuelve una creencia "promising".
- `/review-evidence`, `/extract-insights` y `/analyze-survey` **proponen** las anotaciones; el humano aprueba antes de que se escriba algo.
- Método del curso: la IA propone, el humano decide y la decisión queda registrada (`corrections.md`).

## Fuente

Plugin `afpm` — marketplace `ai-first-skills`, Alaimo Labs. Instalación en Claude Code: `/plugin install afpm`. Licencia CC BY-SA 4.0.
