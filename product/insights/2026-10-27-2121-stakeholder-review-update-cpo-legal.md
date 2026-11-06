---
type: stakeholder-review
date: 2026-10-27
document: product/comms/2026-10-27-2052-update-cpo-legal.md
stakeholders:
  - role: CPO de Teams
    stake: decide si expone la función a 15–20 líderes reales
    knows: lo sigue de lejos
    file: product/stakeholders/cpo-teams.md
  - role: Legal
    stake: evita riesgo de privacidad y residencia de datos
    knows: lo lee por primera vez
    file: product/stakeholders/legal.md
---

# Stakeholder review — update para CPO y Legal (27 de octubre de 2026)

**Documento revisado:** `product/comms/2026-10-27-2052-update-cpo-legal.md` · **Ask:** approval, antes del viernes 7 de noviembre.

Los stakeholders leyeron solo el documento. Lo que el documento no dice, no lo saben. Este ensayo es preparación, no evidencia: no anota ninguna creencia de `product/overview.md`.

---

### CPO de Teams · decide si expone la función a 15–20 líderes reales

**Primera reacción:** El problema está bien probado y lo agradezco. Pero me pedís un OK condicionado a una prueba que todavía no pasó, y el documento no me dice qué significa "pasar".

**Preguntas que haría en la reunión:**
- ¿Cuál es el umbral de la prueba de campo del 31 de octubre? ¿Cuántos líderes confirman la lista, cuántas veces, y qué número la hace fallar?
- ¿Qué mido durante las 4 semanas con los 15–20 líderes? ¿Qué resultado me hace cortar a la semana 2?
- ¿Cuánto cuesta esto? Gente, semanas de ingeniería, y qué dejamos de hacer en Reuniones mientras tanto.
- Los 10 entrevistados, ¿son de una cuenta o de varias? ¿Son representativos del 5% de cuentas grandes?
- "Nadie vende decisiones con dueño": ¿nadie lo vende o nadie lo compra? ¿Qué pasó con Copilot recap, que ya tenemos y 6 de 10 abandonan?

**Qué me falta para decidir:**
- Los criterios de éxito y de corte de la exposición, escritos antes de empezar.
- El costo de la exposición y el equipo asignado.
- Qué pasa si la prueba del 31 no pasa: ¿se cierra la oportunidad o se cambia la solución?
- Un plan para que la exposición no dependa del resultado de IT en noviembre. Si IT no paga, ¿igual tiene sentido construirlo como mejora del plan base?

**Qué me preocupa u objetaría:**
- Pedís aprobar antes de tener el resultado de la prueba de campo. Prefiero decidir el 3 de noviembre con el resultado en la mano, no el 27 de octubre con una condición.
- La creencia de viabilidad (IT paga Max) no tiene evidencia, y es la que sostiene la narrativa de negocio. Exponer a 15–20 líderes no la ataca.
- El recap de IA actual ya falló con estos usuarios. Quiero saber por qué esta lista no corre el mismo riesgo.

**Qué hago con el pedido:** `ask-for-more` · Aprobaría la exposición con el resultado de la prueba del 31 y los criterios de corte en el documento; sin eso, firmo una condición que no puedo evaluar.

---

### Legal · evita riesgo de privacidad y residencia de datos

**Primera reacción:** El documento me da tres líneas y me pide una revisión en diez días. No sé qué datos guarda el registro, dónde, por cuánto tiempo, ni quién los lee.

**Preguntas que haría en la reunión:**
- El registro guarda "nombres, compromisos y motivos". ¿Son datos personales de empleados del cliente? ¿Quién es el responsable del tratamiento, el cliente o Microsoft?
- ¿El registro vive dentro del tenant del cliente, igual que el chat y las notas, o en un servicio nuevo? Si es nuevo, ¿hereda los compromisos de residencia de datos de M365?
- Las grabaciones de la prueba de campo: ¿quién las guarda, hasta cuándo, y quién las borra? "No salen del tenant o se anonimizan" son dos cosas distintas. ¿Cuál aplica?
- ¿Cómo se registra el consentimiento de todos los participantes? ¿Qué pasa con quien entra tarde a la reunión?
- ¿El registro es editable o borrable? Un "motivo" escrito por el líder puede afectar a un tercero. ¿Ese tercero puede objetar o pedir corrección?
- Los 15–20 líderes de la exposición, ¿son clientes reales con contrato? ¿Ya existe un acuerdo de preview o hay que firmar uno?

**Qué me falta para decidir:**
- Una lista de los campos exactos del registro y su clasificación de datos.
- Dónde se almacena, con qué retención y quién puede leer, para la exposición y para el producto final.
- Qué cuentas participan y en qué jurisdicción. "Pagos, EEE" aparece como abierto, pero no sé si alguna cuenta de la exposición cae ahí.
- El mecanismo de consentimiento y de borrado de la prueba de campo, por escrito.

**Qué me preocupa u objetaría:**
- El plazo. Una revisión de residencia de datos para EEE y sector pagos no se hace en diez días sin los datos de arriba.
- "Rastro auditable" es una promesa fuerte. Si el producto lo vende como registro auditable, el cliente va a tratarlo como prueba. Eso cambia la retención y el nivel de integridad que hay que garantizar.
- Que la exposición a líderes reales empiece antes de que yo termine la revisión. El documento no dice si una cosa espera a la otra.

**Qué hago con el pedido:** `ask-for-more` · Puedo arrancar la revisión, pero no puedo entregarla el 7 de noviembre con lo que hay en el documento. Necesito campos, almacenamiento, cuentas y jurisdicciones.

---

## Fuera de personaje — qué cambiaría más su reacción

**Para el CPO:**
1. Agregar el umbral de la prueba de campo del 31 (qué número la hace pasar o fallar) y los criterios de corte de la exposición de 4 semanas. Hoy aprueba a ciegas.
2. Agregar costo y equipo de la exposición, y qué se posterga en Reuniones.
3. Explicar en una línea por qué "Cierre confirmado" no repite el fracaso del recap de IA: el líder confirma, la IA no decide.

**Para Legal:**
1. Agregar una tabla corta: campo del registro · tipo de dato · dónde vive · retención · quién lee. Sin esto, la revisión no empieza.
2. Aclarar la secuencia: la exposición espera la revisión legal, o arranca solo con cuentas fuera de EEE y pagos.
3. Resolver la ambigüedad "no salen del tenant **o** se anonimizan" y decir quién borra las grabaciones y cuándo.

**Síntesis:**
- **Coinciden** en que el documento pide decisiones antes de dar los datos para tomarlas: el CPO no tiene el umbral de la prueba, Legal no tiene los campos del registro. Los dos devuelven `ask-for-more` por falta de información, no por desacuerdo.
- **Tensión 1 — fechas:** el CPO prefiere decidir el 3 de noviembre con el resultado de la prueba en mano. Legal dice que no llega al 7 de noviembre con lo que hay. Si la exposición espera a ambos, se corre; si no espera a Legal, el CPO aprueba algo que Legal puede frenar después.
- **Tensión 2 — "rastro auditable":** para el CPO es la narrativa que justifica Max. Para Legal es la promesa que sube la exigencia de retención e integridad. Cuanto más fuerte se vende al CPO, más caro se hace para Legal. Conviene decidir antes de la reunión si la exposición habla de "registro" o de "rastro auditable".

**Próximo paso:** revisar el update y correr `/stakeholder-review` de nuevo con los mismos dos stakeholders.
