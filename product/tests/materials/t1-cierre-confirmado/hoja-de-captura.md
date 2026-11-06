---
test: T1 cierre-confirmado
tests: product/tests/2026-10-06-2043-la-reunion-no-cierra.md
piece: capture-sheet
---

# Hoja de captura — una por reunión

Se llena en tres momentos: en la reunión, al día siguiente y a los 7 días. Nada más que lo que está acá: sin encuesta de satisfacción, sin preguntas de "¿te gustó?".

## Participante

| Campo | Valor |
|---|---|
| Líder (código) | |
| Provenance | real (Team Lead del pool) / synthetic (compañero de cursada o rol actuado) |
| Origen en el pool | entrevistado antes / nuevo del pool / variante datos / no sale de Teams |

## Reunión

| Campo | Valor |
|---|---|
| Fecha | |
| Tipo de reunión | |
| Participantes (nº) | |
| Herramienta de trabajo usada en la reunión | |
| Grabada con consentimiento de todos (para T2) | sí / no |
| ¿Se tomó al menos una decisión? | sí / no → si no, la reunión no cuenta |

## Cierre (S1)

| Campo | Valor |
|---|---|
| Nº de decisiones listadas | |
| Huecos en blanco | dueño: __ · fecha: __ · motivo: __ |
| Resultado del cierre | confirmó tal cual / corrigió y confirmó / pospuso / ignoró |
| Si pospuso: ¿confirmó dentro de las 24 h? | sí / no |
| Minutos del cierre | |
| Leída en voz alta al equipo | sí / no |
| Qué corrigió (si corrigió) | |

## Día siguiente (S2)

| Campo | Valor |
|---|---|
| Reescritura | no / sí, misma lista copiada / sí, contenido distinto |
| Dónde (ticket, correo, recap, canal) | |
| Artefacto adjunto | [archivo o captura] |
| Qué difiere de la lista confirmada | |

## Día 7 (S3)

| Campo | Valor |
|---|---|
| Respuesta literal | |

---

# Resumen del campo — una vez, al cierre

| Reunión | Líder | Provenance | Fecha | ¿Decidió? | Resultado del cierre | Confirmó en 24 h (si pospuso) | Minutos | Voz alta | Reescritura | Respuesta día 7 |
|---|---|---|---|---|---|---|---|---|---|---|
| R01 | | | | | | | | | | |
| R02 | | | | | | | | | | |
| … | | | | | | | | | | |

## Lectura

Solo con filas `real`. Las `synthetic` se reportan aparte y no mueven la creencia #11.

- Reuniones que cuentan (con al menos una decisión): __ → si < 10, el test es `inconclusive`.
- **S1** = (confirmó tal cual + corrigió y confirmó) / reuniones que cuentan = __ / __ → umbral ≥ 2/3. "Pospuso" e "ignoró" cuentan como no confirmada.
- **S2** = reuniones confirmadas sin registro aparte con contenido distinto / reuniones confirmadas = __ / __ → umbral ≥ 2/3. Copiar la misma lista a Jira o al canal no es reescritura.
- **S3** = reuniones con algo ejecutado distinto o reabierto a los 7 días = __ (se reporta, no decide).
- Pospuso y confirmó dentro de las 24 h = __ (alimenta la regla de `change` asíncrono).
- Minutos del cierre, mediana = __ (alimenta la creencia `[usability]` de A1; no decide aquí).

La regla de decisión es la del archivo de tests. No se cambia aquí.
