---
source: secondary
method: web
date: 2026-09-16
question: Qué han hecho Zoom, Google Meet y Miro/Mural/FigJam con la colaboración dentro de la videollamada, en qué plan lo cobran y si hay evidencia de adopción — para decidir si "trabajo en vivo dentro de la reunión" puede vivir en Max o si el mercado ya lo volvió commodity de plan base.
opportunity: trabajo-en-vivo-fuera-de-teams
---

# Research: colaboración en vivo dentro de la videollamada — competidores, alternativas, packaging y tendencias

Método: búsqueda web con cuatro agentes en paralelo (competidores directos, alternativas y foros, pricing y packaging, tendencias y adopción), 2026-09-16. Cada hecho lleva su etiqueta de procedencia: `[verificado: URL — fecha]` o `[conocimiento del modelo — verificar]`. Límites de la corrida: Reddit no fue accesible (el sentimiento sale de Microsoft Tech Community y G2); las páginas de precios de Zoom y Google no se pudieron abrir directo y se usaron fuentes secundarias marcadas como tales; los reportes de tool sprawl (Okta, Productiv, Zylo) no se pudieron leer. Dos datos quedaron con procedencia dudosa y están marcados.

**Lo que cambia decisiones.** Primero, la colaboración en vivo básica dentro de la llamada (pizarra, notas, votaciones) ya es plan base o medio en el mercado: Zoom la incluye desde el plan gratis y Meet desde Business Standard; lo que sí se vende en el escalón superior es el control de IT sobre esa colaboración — seguridad, cumplimiento, IA — que es exactamente lo que empaqueta Teams Premium a USD 10 por usuario. "Colaboración en vivo" sola no sostiene los USD 8 de Max. Segundo, Google decidió no construir la pizarra: mató Jamboard y delegó el whiteboarding a Miro, FigJam y Lucid dentro de Meet, y Microsoft empuja lo mismo con Live Share y Mural como ISV dentro de la reunión; aparece una tercera respuesta que el brief no tenía — traer el tablero externo adentro de la reunión sin fricción, en vez de reemplazarlo. Tercero, nadie publica cifras de adopción de colaboración en vivo (ni Zoom Whiteboard, ni Zoom Docs, ni Microsoft Whiteboard, ni Loop), pero la fricción del Whiteboard nativo está documentada en canales oficiales de Microsoft y en reseñas; la telemetría propia (6% de apertura, la mitad abandona antes de dos minutos) es probablemente el mejor dato que existe sobre esto y el mercado no la va a reemplazar.

## Competidores directos: qué existe dentro de la llamada

### Zoom

Zoom Whiteboard vive dentro de la reunión: herramientas de dibujo, más de 250 plantillas, generación de tableros con IA desde transcripciones, comentarios enhebrados, exportación a PDF/imagen/PPT. El plan gratis (Basic) incluye 3 tableros editables simultáneos; Whiteboard Plus (ilimitados + IA) cuesta desde USD 2,07 por usuario por mes o viene incluido en Zoom Workplace Business, Business Plus y Enterprise Essentials `[verificado: https://www.zoom.com/en/products/online-whiteboard/ — 2026-09-16]`.

Zoom Docs es un documento colaborativo co-editable en tiempo real que se abre desde el panel lateral de la reunión ("Open Docs in the meeting... and co-edit in real time"), con resúmenes organizados automáticamente por AI Companion; incluido en cuentas pagas de Zoom Workplace, con las funciones de IA completas atadas a un add-on con créditos medidos `[verificado: https://www.zoom.com/en/products/collaborative-docs/features/meetings-collaboration/ — 2026-09-16]` `[verificado: https://www.zoom.com/en/blog/zoom-docs-ai-powered-adaptive-workspace/ — 2026-09-16]`. Un agente reportó un renombre de "Zoom Docs" a "Zoom Canvas" a partir de una nota japonesa de junio de 2026 sin confirmación en fuente primaria — `[conocimiento del modelo — verificar]`. Fecha de lanzamiento de Docs y cifras de adopción: desconocido.

Polls y anotación sobre pantalla compartida en Zoom: no verificados en esta corrida — desconocido.

### Google Meet

Google no tiene pizarra propia: Jamboard dejó de permitir creación y edición el 1 de octubre de 2024 y se apagó el 31 de diciembre de 2024; Google decidió no construir un sustituto e integró terceros — FigJam, Lucidspark, Miro — "across Google Workspace", incluida la colaboración durante llamadas de Meet `[verificado: https://workspaceupdates.googleblog.com/2023/09/the-next-phase-of-digital-whiteboarding-for-google-workspace.html — 2026-09-16]`. En mayo de 2026 seguía ampliando esa estrategia con add-ons de whiteboarding para hardware de salas Meet `[verificado: https://workspaceupdates.googleblog.com/2026/05/whiteboarding-add-ons-meet-hardware-android.html — 2026-09-16, solo título]`.

Polls son función nativa de Meet desde Workspace Essentials y Business Standard en adelante; no en el plan gratis personal `[verificado: https://support.google.com/meet/answer/10165071?hl=en — 2026-09-16]`. Q&A existe como función separada; plan mínimo desconocido. Anotación nativa sobre pantalla compartida: no confirmada en fuente de Google, solo apps de marketplace `[conocimiento del modelo — verificar]`. Panel de Docs co-editable embebido en la llamada: desconocido. La apuesta de Meet con Gemini es post-reunión: notas automáticas y "próximos pasos" sugeridos después de la llamada, no co-creación durante `[verificado: https://www.techradar.com/pro/google-meet-will-now-use-gemini-to-suggest-next-steps-after-your-team-meetings — 2026-09-16]`.

### Microsoft Teams (para contraste)

Collaborative meeting notes como componente Loop dentro de la reunión: agenda, notas y action items co-creados; documentado en agosto de 2024, plan mínimo y fecha exacta de lanzamiento no extraíbles del fetch — desconocido `[verificado: https://techcommunity.microsoft.com/blog/microsoft365insiderblog/collaborative-meeting-notes-in-teams-meetings/4220383 — 2026-09-16, metadatos]`. La prensa anticipa más "Loop Meeting Notes" en 2026 `[verificado: https://windowsreport.com/microsoft-teams-will-add-loop-meeting-notes-and-branded-reactions-in-2026/ — 2026-09-16, solo título]`.

PowerPoint Live, Whiteboard y Excel Live en reuniones con watermark llegaron a Teams Premium en febrero de 2024 `[verificado: https://m365admin.handsontek.net/powerpoint-live-whiteboard-and-excel-live-for-watermarked-meetings-premium/ — 2026-09-16]`. La tabla de planes de Microsoft no desglosa qué funciones de reunión están en cada tier; menciona "Whiteboard and collaborative annotations" de forma genérica `[verificado: https://www.microsoft.com/en-us/microsoft-teams/compare-microsoft-teams-business-options — 2026-09-16]`. Plan mínimo de PowerPoint Live y Excel Live sin watermark: desconocido `[conocimiento del modelo — verificar: existirían desde el plan base]`.

Microsoft lanzó Live Share el 24 de mayo de 2022: SDK para que apps de terceros dentro de una reunión de Teams sean "multijugador" con sincronización de estado, anotación en tiempo real y control por rol `[verificado: https://devblogs.microsoft.com/microsoft365dev/introducing-live-share-interactive-app-experiences-in-microsoft-teams-meetings/ — 2026-09-16]`, y promociona a Mural como ISV que "increase revenue and retain customers on Microsoft Teams" con ese marco `[verificado: https://www.microsoft.com/en-us/microsoft-365/blog/2023/04/10/4-ways-isvs-like-mural-increase-revenue-and-retain-customers-on-microsoft-teams/ — 2026-09-16, solo título]`.

### Tabla comparativa

| Función | Zoom | Google Meet | Microsoft Teams |
|---|---|---|---|
| Pizarra nativa en la llamada | Sí — Basic gratis (3 tableros); ilimitada desde Business o add-on Plus USD 2,07 | No — delegado a FigJam/Lucidspark/Miro | Sí — Whiteboard; con watermark requiere Premium |
| Documento colaborativo embebido | Sí — Zoom Docs, cuentas pagas | Desconocido | Sí — Loop / Collaborative notes; plan mínimo desconocido |
| Anotación sobre pantalla compartida | Desconocido | Sin función nativa confirmada | Sí, genérica; plan desconocido |
| Polls / votaciones | Desconocido | Sí — desde Essentials / Business Standard | Desconocido |
| Apps de terceros dentro de la reunión | Desconocido | Sí — marketplace (FigJam, Lucid, Miro) | Sí — Live Share / meeting apps; plan mínimo desconocido |
| Cobro de la pizarra avanzada | USD 2,07/usuario/mes o Business+ | N/A (terceros) | Premium para el caso con watermark; base desconocido |

## Alternativas: cómo entraron Miro, Mural y FigJam a la reunión

| Proveedor | Plataforma | Qué permite en la reunión | Editar sin cuenta | Plan del proveedor | Requisito del lado Microsoft/Google |
|---|---|---|---|---|---|
| Miro | Teams | Tableros embebidos en reuniones, canales, chats e invitaciones; notificaciones en vivo | No especificado; "permission and access settings will vary based on plan type" | Free, Starter, Business, Education, Enterprise y "all Microsoft 365 plans" | Admin habilita la app desde el catálogo; con sharing restringido algunas opciones no están `[verificado: https://help.miro.com/hc/en-us/articles/4406387211538-Miro-for-Microsoft-Teams-user-guide y https://help.miro.com/hc/en-us/articles/4406387610002-Miro-for-Microsoft-Teams-admin-guide — 2026-09-16]` |
| Miro | Zoom | App de Miro para Zoom desde julio de 2021 | Desconocido | Desconocido | Desconocido `[verificado: https://www.businesswire.com/news/home/20210721005601/en — 2026-09-16]` |
| Miro | Meet | Integración en disponibilidad general | Desconocido | Desconocido | Desconocido `[verificado: https://workspace.google.com/blog/product-announcements/a-new-integration-of-google-meet-and-miro-is-now-in-general-availability — 2026-09-16, solo título]` |
| Mural | Teams | "Share-to-stage": el mural en el escenario de la reunión en tiempo real | No especificado | Incluida en todos los planes de Mural | Admin permite instalar desde el App Store de Teams; sin licencia extra de Teams `[verificado: https://www.mural.co/blog/mural-app-for-microsoft-teams — 2026-09-16]` |
| FigJam | Meet | Presentar archivos y prototipos sin screen-share tradicional, colaboración en tiempo real | Sí: "open session to temporarily invite anyone to edit the FigJam file, including those without Figma accounts" | Todos los planes | Sin plan mínimo especificado `[verificado: https://help.figma.com/hc/en-us/articles/16921722048151-Figma-and-Google-Meet — 2026-09-16]` |

Lo que esto prueba: las tres herramientas ya tienen un camino oficial para vivir dentro de la reunión de Teams o Meet, y Microsoft lo promueve. Lo que no prueba: que la organización de Valeria las haya elegido por frustración con Teams; pudo elegirlas por estándar de diseño o licencia previa y traerlas a la llamada como una instancia más de su uso diario. Ninguna fuente mide el momento "a mitad de la llamada".

### Sentimiento de usuarios (señal, no hecho)

En el propio Microsoft Tech Community, la fricción de invitados con el Whiteboard es recurrente: "the client couldn't see the chat function nor the whiteboard" (2020), con la respuesta de que el invitado debía "switch over to your tenant prior or before the meeting" `[verificado: https://techcommunity.microsoft.com/t5/microsoft-teams/external-guest-don-t-have-chat-can-t-see-whiteboard/td-p/1810859 — 2026-09-16]`; "As a guest in a few organizations & I'm unable to start a whiteboard in any of them" (2023), y habilitarlo requiere que un admin active guest access con "Create and edit" a nivel de equipo — no es self-service para el usuario `[verificado: https://techcommunity.microsoft.com/discussions/microsoftteams/guests-cant-share--create-whiteboard/3812702 — 2026-09-16]`.

Reseñas de Microsoft Whiteboard en G2 `[verificado: https://www.g2.com/products/microsoft-whiteboard/reviews — 2026-09-16]`: "It takes forever to load! It froze often as well" (2020); "some times syncing between devices is with delay and error" (2021); "when two or more people are writing... one can see only one piece of data at a time" (2023); "Limited shapes and colors, very limited template selection, no integrations with common tools like Jira" (2024); "not as powerful or capable as other options such as miro" (2024).

Shadow IT de Miro/Notion con tarjeta corporativa: patrón ampliamente discutido pero sin dato cuantitativo verificado en esta corrida `[conocimiento del modelo — verificar]`.

## Pricing y packaging

| Proveedor | Tier | Precio/usuario/mes | Colaboración en reunión incluida |
|---|---|---|---|
| Zoom Workplace | Basic | USD 0 | 40 min, 100 participantes, 3 pizarras, 3 notas IA/mes |
| Zoom Workplace | Pro | USD 14,16 | Notas IA ilimitadas |
| Zoom Workplace | Business | USD 18,33 | 300 participantes, pizarras ilimitadas |
| Zoom Workplace | Business Plus | USD 24,50 | Business + telefonía |
| Zoom Workplace | Enterprise | Custom | 500+ participantes `[verificado (fuente secundaria): https://meetgeek.ai/blog/zoom-price-plans — 2026-09-16]` |
| Google Workspace | Business Starter | USD 7 anual / 8,40 mensual | Meet 100, sin grabación |
| Google Workspace | Business Standard | USD 14 / 16,80 | Meet 150, grabación, polls |
| Google Workspace | Business Plus | USD 22 / 26,40 | Meet 500, Gemini más amplio |
| Google Workspace | Enterprise | Custom | Meet 1.000, streaming `[verificado (fuente secundaria): https://www.emailtooltester.com/en/blog/google-workspace-pricing/ — 2026-09-16]` |
| Microsoft | Teams Premium (add-on) | USD 10 | Cifrado E2E, watermarking, recap con IA, traducción en vivo, branding `[verificado: https://www.microsoft.com/en-us/microsoft-teams/premium — 2026-09-16]` |
| Microsoft | "Business Max" | — | No existe públicamente; construcción del caso. El análogo real de "USD 8 más por usuario por reuniones avanzadas" es Teams Premium `[verificado ausencia: microsoft.com/premium — 2026-09-16]` |
| Microsoft | Whiteboard / Loop | Incluidos según plan | Loop básico para "cualquiera con acceso a Teams, Outlook, Word Online, Whiteboard"; Copilot en Loop requiere licencia Copilot; tiers exactos no enumerados `[verificado parcial: https://support.microsoft.com/en-us/office/loop-access-via-microsoft-365-subscriptions-92915461-4b14-49a4-9cd4-d1c259292afa — 2026-09-16]` |
| Miro | Starter / Business / Enterprise | USD 8 / 20 / custom | Visitor editing desde Starter; guests ilimitados desde Business; integración Teams/Zoom no mencionada en pricing `[verificado: https://miro.com/pricing/ — 2026-09-16]` |
| Mural | Team+ / Business / Enterprise | USD 9,99 anual (12 mensual) / 17,99 / custom | Integraciones Zoom/Webex y visitantes con edición desde Team+; guests desde Business `[verificado: https://www.mural.co/pricing — 2026-09-16]` |
| FigJam | Free / Professional / Org-Enterprise | USD 0 / 3 / 5 | Viewers siempre gratis `[verificado (fuente secundaria): https://costbench.com/software/diagramming/figjam/ — 2026-09-16]` |

Evidencia de que la colaboración en reuniones motive upgrade o churn: en un earnings call de Zoom, el CFO atribuye subas de precio con "record low churn" a "workplace portfolio as well as AI" y el CEO cita "chat, calendar, meetings, whiteboard... as well as AI value", sin separar whiteboard o Docs `[verificado: https://www.fool.com/earnings/call-transcripts/2026/05/25/zoom-zm-q4-2026-earnings-call-transcript/ — 2026-09-16; la fecha de la URL no cierra con el calendario fiscal de Zoom — verificar]`. Okta Businesses at Work 2026 no expone cifras de apps por empresa ni redundancia en la parte accesible `[verificado parcial: https://www.okta.com/newsroom/articles/businesses-at-work-2026/ — 2026-09-16]`; Productiv y Zylo: desconocido.

Lectura del lane: la colaboración en vivo básica está en planes de entrada o medios; lo que se concentra en tiers superiores o add-ons es pizarra ilimitada, IA sin tope, grabación, guests ilimitados y, en Microsoft, seguridad y cumplimiento sobre la reunión. No se puede concluir qué parte de upgrades o churn reales se debe a colaboración en reunión versus IA o precio.

## Posicionamiento y tendencias

| Player | Mensaje | A quién apunta |
|---|---|---|
| Zoom | "One platform for all the ways you work"; "AI-first work platform"; explícitamente contra el app-switching `[verificado: https://www.zoom.com/en/products/collaboration-tools/ y https://news.zoom.com/zoomtopia-2024-unveiling-ai-first-work-platform-innovations/ — 2026-09-16]` | Consolidación de herramientas, mid-market y enterprise |
| Microsoft | Teams + Copilot, "your copilot for work" `[verificado: https://seekingalpha.com/pr/19204335-introducing-microsoft-365-copilot-your-copilot-for-work — 2026-09-16]`; tagline "the app for work" no confirmada | Base instalada de M365; agentes e IA en el flujo |
| Google | Meet + Gemini: notas y próximos pasos post-reunión `[verificado: https://www.techradar.com/pro/google-meet-calls-will-now-automatically-take-notes-for-you — 2026-09-16]` | Usuarios de Workspace; "mejores reuniones" vía IA después |
| Miro | "The Innovation Workspace" `[verificado: https://miro.com/innovation-workspace/ — 2026-09-16]` | Producto, diseño, innovación |
| Mural, FigJam | Desconocido (no buscado) | Desconocido |

Espacio saturado: notas y resúmenes con IA — tratado como commodity entre Zoom, Teams y Meet por múltiples comparativas de blogs de producto `[verificado (señal, baja calidad): https://fellow.ai/blog/ai-meeting-summary-tools/ y https://www.usecarly.com/blog/best-ai-note-takers-zoom-teams-meet/ — 2026-09-16]`. Vacío aparente: colaboración estructurada en vivo dentro de la llamada para grupos grandes, con adopción demostrada — ningún jugador la reclama `[conocimiento del modelo — verificar]`.

Adopción: Miro reportó 50 millones de usuarios y el 99% del Fortune 100 en marzo de 2023, el dato duro más reciente encontrado `[verificado: https://miro.com/newsroom/miro-recognizes-50-million-minds-on-their-way-to-the-next-big-thing/ — 2026-09-16]`. Zoom Whiteboard, Zoom Docs, Microsoft Whiteboard y Loop: sin cifras públicas — desconocido. Jamboard es la señal de que una pizarra standalone de un big player no sobrevivió `[verificado: https://9to5google.com/2023/09/28/google-jamboard/ — 2026-09-16]`.

Contexto sobre reuniones grandes: Atlassian "State of Meetings" (n=5.000 trabajadores del conocimiento) — 72% de las reuniones consideradas inefectivas, 78% dice que le cuesta completar su trabajo por exceso de reuniones `[verificado: https://fortune.com/2024/03/21/meetings-productivity-ineffective-atlassian-report — 2026-09-16]`. Tiempo perdido específicamente por fricción tecnológica (enlaces, permisos, cambio de herramienta): ningún dato con fuente primaria y n — desconocido. Microsoft Work Trend Index 2026: sin cifras sobre esto en la página accesible.

## Impacto en creencias

| Creencia (de overview.md) | Veredicto | Evidencia |
|---|---|---|
| #1 [opportunity: trabajo-en-vivo-fuera-de-teams] [value] Sale de Teams porque colaborar en vivo adentro no le sirve y el desvío le cuesta tiempo y rastro — no porque la org ya eligió Miro/Mural/FigJam | Apoya parcialmente, no resuelve | La fricción del Whiteboard nativo está documentada (guest access que requiere admin, rendimiento, un trazo a la vez, comparación desfavorable con Miro) — apoya el "no le sirve". Pero Miro y Mural tienen integración oficial dentro de la reunión de Teams, así que la org pudo elegirlas antes y solo traerlas a la llamada. Ninguna fuente mide el momento "a mitad de la llamada" ni el costo en minutos. Sigue en primario. |
| #2 [product] [value] Los enlaces externos en el 29% son síntoma de que notas/Whiteboard no sirven para trabajar en vivo con 8+ | Apoya parcialmente | Mismas fuentes que #1. Nada en el mercado distingue reuniones de 8+. |
| #3 [opportunity: trabajo-en-vivo-fuera-de-teams] [viability] IT reconoce la colaboración en vivo como capacidad que justifica Max; la fuga a herramientas externas pesa en su renovación | Contradice la primera mitad; no dice nada de la segunda | La colaboración en vivo básica es plan base o medio en Zoom y Meet; lo que se cobra en el escalón superior es control de IT sobre ella — seguridad, cumplimiento, IA (Teams Premium USD 10). Sobre si la fuga pesa en renovación: sin evidencia pública; tool sprawl no accesible. |
| #4 [product] [value] El "ya usa otras herramientas" del churn refiere a Miro/Notion/Slack, no a Zoom/Meet | No dice nada | Ninguna fuente separa motivos de baja por tipo de herramienta. |
| #5 [product] [viability] El Team Lead no puede nombrar hoy una capacidad de reuniones de Max que valga USD 8 | Apoya indirectamente | El mercado tampoco la nombra: Zoom atribuye sus subas a "workplace + IA" sin separar whiteboard; Teams Premium se vende por seguridad e IA, no por reuniones colaborativas. |
| #6 [product] [value] "Demasiadas reuniones" es dolor del convocante; notas 8% es fricción | Apoya débilmente, como contexto | Atlassian n=5.000: 72% inefectivas, 78% no completa su trabajo. General, no sobre notas. |
| #7 [product] [viability] IT sube a Max si ve adopción visible de los Team Leads | No dice nada | Sin evidencia de mercado sobre el criterio de renovación de IT. |

Implicación para la oportunidad (no es una decisión, es lo que la evidencia sugiere): el valor para Max no es "poder colaborar en vivo" — eso el mercado lo regala — sino "colaborar en vivo bajo control de IT" (seguridad, auditoría, rastro que queda). Y la idea "traer Miro/Jira/Power BI adentro de la reunión sin fricción de enlaces y permisos" merece entrar a las ideas candidatas del brief; es la ruta que eligieron Google y el propio Microsoft con Live Share. Ambas cosas las decide `/review-evidence` y `/clarify-idea`, no este archivo.

## Qué sigue necesitando research primario

- **Cuánto cuesta el desvío** (#1, #2): el mercado no tiene un solo dato con n sobre minutos perdidos por enlaces, permisos o cambio de herramienta. Va a la telemetría propia (duración de la caída de actividad, alargamiento de la reunión) y a la encuesta.
- **Por qué se van** — frustración in situ o elección previa de la org (#1): sólo lo distinguen entrevistas a Team Leads sobre el momento exacto en que abren Miro en vez de Whiteboard. Las Whiteboard cerradas en <2 min seguidas de enlace externo (dato propio) son el proxy cuantitativo.
- **Si la fuga pesa en la renovación** y qué nombraría IT frente a Compras (#3, #7): entrevistas a responsables de Collaboration Services; el mercado sugiere que la palabra que vende es "control" (seguridad, auditoría), no "colaboración" — es una hipótesis para probar en la guía, no un hallazgo.
- **Qué significa "ya usa otras herramientas"** en las bajas (#4): datos propios de Ventas o entrevistas de salida; secundario no llega.
- **Variante Gustavo** (dashboards en vivo): no se investigó en esta corrida por decisión del PM; queda abierta.
