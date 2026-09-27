---
status: framed
segment: Team Lead de una cuenta de más de 1.000 licencias de Microsoft 365 que conduce reuniones de 8 o más participantes en las que el grupo tiene que trabajar sobre material (backlog, tablero, documento, dashboard) durante la llamada
personas: valeria-ortiz (primaria), gustavo-ferreyra (secundaria), lucia-benitez (paga el costo, no lo sufre); tomas-iriarte excluido
---

# Opportunity: Trabajo en vivo fuera de Teams

El Team Lead que conduce reuniones de 8+ personas en cuentas grandes tiene que salir de Teams a mitad de la reunión (Miro, Mural, FigJam, Jira, Google Docs, Power BI) para que el grupo trabaje sobre el material, y paga ese desvío con minutos perdidos en enlaces y permisos, con actividad que se va de Teams mientras dura y con un rastro disperso que reconstruye después; el momento es ahora porque "colaboración" ya aparece en las conversaciones de renovación de Max y porque CollabCon, en cinco meses, fija una fecha para decidir qué mostrar.

## Segmento y personas

- **Valeria Ortiz (primaria)** — lo sufre en cada una de sus 6 a 8 reuniones semanales de 8+: comparte pantalla de Jira o Miro, pega el enlace, la mitad no tiene acceso, cinco minutos se van en permisos; Whiteboard le parece un juguete y el resultado "queda perdido"; reconstruir "por qué decidieron esto" le lleva media hora.
- **Gustavo Ferreyra (secundaria)** — variante "datos": comparte el dashboard de Power BI, le piden filtrar o hacer zoom, pega el enlace y la mitad no lo abre por licencia o permiso; pierde ~10 minutos por reunión. Su problema es mirar y anotar sobre los mismos datos, no editar juntos; cualquier solución que solo sirva a Valeria lo deja afuera.
- **Lucía Benítez (terciaria)** — no lo sufre, lo paga: 14 suscripciones a Miro/Notion en tarjetas corporativas, auditoría de herramientas no sancionadas, y un reporte de adopción de Premium que Compras le recuerda en cada renovación. Es quien decide si esto vale USD 8 por usuario.
- **Tomás Iriarte (negativa)** — excluido: participa, no convoca; reuniones chicas; su respuesta al Whiteboard es abrir Figma. Si una idea lo entusiasma a él y no a Valeria, estamos resolviendo el problema equivocado.
- **Persona faltante:** ninguna evidente para este problema. Si la investigación muestra que el desvío lo protagonizan facilitadores de talleres de 15+ personas (y no Team Leads de equipo), convendría una persona para ese rol — `/generate-personas` en ese caso.

## Señales

| Señal | Procedencia | Fuente |
|---|---|---|
| "Colaboración durante reuniones" fue la 3.ª categoría más frecuente del portal de feedback en 12 meses: 4.700 solicitudes del segmento; las más repetidas: editar un documento entre varios durante la llamada, votar o priorizar en vivo, no salir de Teams para una sesión de trabajo | real | Portal de feedback, últimos 12 meses (aportado por el PM) |
| En el 38% de las reuniones del segmento con más de 5 participantes se comparte en el chat un enlace a Miro, Mural o FigJam durante la llamada; mientras dura, la actividad en Teams cae | real | Telemetría del segmento (aportado por el PM) |
| Whiteboard se abre en el 6% de las reuniones del segmento; en la mitad de esas se cierra antes de los dos minutos | real | Telemetría del segmento (aportado por el PM) |
| El 22% de los comentarios negativos post-reunión del segmento menciona la colaboración en vivo: "para hacer algo juntos terminamos en otra herramienta", "la pizarra es difícil de encontrar y nadie la usa", "pierdo tiempo pasando lo que decidimos a un documento después" | survey | Encuestas post-reunión del segmento (n no declarado) |
| En renovaciones de cuentas grandes, "colaboración" aparece en las conversaciones sobre el plan Max | unverified | Ventas; sin registro de cuántas veces |
| En el 29% de las reuniones de más de 5 personas (todo el producto) se comparte un enlace externo; uso de notas 8%, Whiteboard 5%; quejas por colaboración en reunión 19% | unverified | Brief del caso, sin fuente nombrada (product/overview.md) |
| Motivos de baja: "pagamos por funciones que no usamos", costo, "el equipo ya usa otras herramientas"; 2,4% sube de plan, 3,6% baja o no renueva | unverified | Brief del caso (product/overview.md) |
| Valeria: ~5 min por reunión en permisos, ~40 min/semana reescribiendo notas en Notion, media hora para reconstruir una decisión. Gustavo: ~10 min por reunión con el enlace de Power BI. Lucía: 14 suscripciones a Miro/Notion descubiertas en gastos | synthetic | product/personas/ |

Las señales `real` describen el comportamiento (se van, y cuando prueban lo que hay adentro lo abandonan en dos minutos); todavía no dicen **cuánto cuesta** el desvío ni **por qué** se van — eso es lo que la agenda de investigación tiene que cerrar.

## Resultado de negocio

Comercial. Métricas que mira la dirección para este segmento: **tasa de upgrade a Max** (hoy 2,4% de las cuentas sube de plan), **retención en la renovación** (94%; 3,6% baja o se va) e **ingresos por licencia** (Max suma USD 8 por usuario por mes). La oportunidad sirve al outcome si la colaboración en vivo se vuelve una capacidad de reunión que IT puede nombrar frente a Compras para justificar Max, y si reduce el "el equipo ya usa otras herramientas" que hoy motiva bajas.

## Restricciones

- Presupuesto máximo: USD 5M.
- Las features se presentan en CollabCon, dentro de 5 meses (≈ mediados de febrero de 2027). Fija la fecha de las decisiones de la agenda, no el alcance de la solución.
- Límites para cualquier solución futura (hechos, no decisiones): facilidad de uso, accesibilidad, compatibilidad con Microsoft 365, privacidad y seguridad corporativas, tiempo real, impacto mínimo en el rendimiento de la reunión.
- Contexto de compra: contrata y despliega IT; el Team Lead no elige la herramienta. Cualquier valor tiene que ser visible en los reportes de adopción que IT muestra al CFO.

## Creencias

Referencian `product/overview.md`, el único registro. Las dos nuevas refinan creencias ya registradas y se proponen para el registro; las existentes se citan por número.

- [opportunity: trabajo-en-vivo-fuera-de-teams] [value] El Team Lead sale de Teams porque colaborar en vivo dentro no le sirve, y ese desvío le cuesta tiempo medible por reunión (permisos, enlaces, retomar el ritmo) y un rastro que reconstruye después — no porque su organización ya haya elegido Miro, Mural o FigJam por otros motivos. *(refina la #4 del registro con el 38% de enlaces y la caída de actividad)*
- [opportunity: trabajo-en-vivo-fuera-de-teams] [viability] IT reconoce la colaboración en vivo dentro de la reunión como una capacidad nombrable que justifica Max frente a Compras, y la fuga a herramientas externas (gasto, auditoría) pesa en su decisión de renovación. *(refina la #5 y la #8 del registro)*
- [opportunity: trabajo-en-vivo-fuera-de-teams] [viability] Lo que IT pagaría en Max no es colaborar en vivo sino colaborar en vivo bajo control de IT (seguridad, auditoría, rastro que queda). *(#3 del registro; agregada el 2026-09-22 a partir de product/research/2026-09-16-1313-colaboracion-en-vivo-dentro-de-la-videollamada.md)*
- Relacionadas ya registradas: #6 (el "ya usa otras herramientas" del churn refiere a herramientas alrededor de la reunión) y #7 (el 8% de notas es fricción, no falta de necesidad).

## Agenda de investigación

Ordenada por costo. Cada fila dice qué decisión destraba y cuándo hace falta, con CollabCon como fecha límite dura.

| Creencia                                      | Instrumento                                                                                                                                                                                                                                                    | Decisión que destraba                                                                                                                                          | Para cuándo                         |
| --------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| [value] — cuánto cuesta el desvío             | **Datos propios**: sobre la telemetría del 38%, medir cuánto dura la caída de actividad, si la reunión se alarga respecto de las que no comparten enlace, y si la caída ocurre también con enlaces a Docs/Jira/Power BI (variante Gustavo) o solo con tableros | Si el desvío es corto y la reunión no se alarga, el problema es menor de lo que dicen las 4.700 solicitudes y la oportunidad se achica a "rastro disperso"     | 2 semanas (finales de septiembre)   |
| [value] — abandono de lo que existe           | **Datos propios**: de las Whiteboard cerradas antes de 2 minutos, cuántas terminan con un enlace externo en el chat en los 5 minutos siguientes                                                                                                                | Confirma o refuta que se van *por* la herramienta interna, no *a pesar* de ella                                                                                | 2 semanas                           |
| [viability] — Max y colaboración              | **Datos propios**: cruzar cuentas grandes que subieron a Max o bajaron en los últimos 12 meses con su tasa de enlaces externos y con menciones de "colaboración" en notas de Ventas                                                                            | Si las cuentas que se van son las que más enlaces comparten, la viabilidad tiene base; si no, la oportunidad puede ser de retención de uso pero no de ingresos | 3 semanas                           |
| [value] + [viability]                         | `/research-market`: qué han hecho Zoom, Google Meet, Miro/FigJam/Mural con la colaboración dentro de la videollamada, en qué plan lo cobran, y si hay evidencia de adopción                                                                                    | Decide si la capacidad puede vivir en Max o si el mercado ya la volvió commodity de plan base                                                                  | 4 semanas (mediados de octubre)     |
| [value] — cuántos, cuánto, con qué frecuencia | `/design-survey` a Team Leads del segmento: frecuencia del desvío, minutos perdidos, herramienta destino, qué hacen con el resultado después; bloque de opt-in para entrevistas                                                                                | Dimensiona el problema con n declarado y reemplaza el 22% sin n; define el pool de entrevistas                                                                 | 7 semanas (principios de noviembre) |
| [viability] — la voz de IT                    | `/design-interview` con responsables de Collaboration Services (perfil Lucía) de cuentas grandes: cómo justifican Max, qué peso tiene la fuga a herramientas externas, qué reporte de adopción los convencería                                                 | Decide si el outcome es upgrade o solo retención, y qué debe medir cualquier solución para que IT lo vea                                                       | 9 semanas (mediados de noviembre)   |
| [value] — el porqué                           | `/design-interview` con Team Leads del opt-in, priorizando los que dijeron que el desvío no les cuesta                                                                                                                                                         | Cierra o descarta la oportunidad; si cierra, habilita `/clarify-idea` con tres meses para CollabCon                                                            | 10 semanas (fines de noviembre)     |

## Ideas candidatas (no evaluadas)

- "Herramientas colaborativas integradas" en la reunión — la dirección con la que llegó el pedido; estacionada, no elegida.
- Editar un documento entre varios durante la llamada; votar o priorizar en vivo — pedidas literalmente en el portal de feedback; se registran como lo que el usuario pide, no como lo que se va a construir.
- Traer Miro, Jira o Power BI adentro de la reunión sin fricción de enlaces y permisos, en vez de reemplazarlos — la ruta que eligieron Google (terceros en Meet) y Microsoft (Live Share, Mural); agregada el 2026-09-22 desde product/research/2026-09-16-1313-colaboracion-en-vivo-dentro-de-la-videollamada.md.
- Trabajar sobre el dashboard compartido (filtrar, anotar compromisos sobre los datos) sin salir de la pantalla — variante Gustavo.
- Que el resultado de la sesión en vivo quede en un lugar que el equipo vuelve a mirar — se cruza con la #7 del registro y con la oportunidad "las decisiones se pierden al salir", no enmarcada.
