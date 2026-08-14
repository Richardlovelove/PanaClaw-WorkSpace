# Canal · WhatsApp

Donde termina casi todo el recorrido. No es un canal de difusión: es donde se
cierra.

---

## La regla del número

> **El número no se imprime nunca.** Los botones dicen «WhatsApp», sin dígitos.

Es una decisión de marca del sitio: el número aparece cuando la persona ya está
dentro de la conversación, no como reclamo público.

**El enlace se compone así**, con los valores de
[`datos/marca.json`](../../datos/marca.json) → `contacto`:

```
https://wa.me/19406046565?text={mensaje-codificado-en-url}
```

**Mensaje por defecto:** `Hola PanaClaw, quiero cotizar mi sitio web`

---

## Mensajes precargados por origen

Cada botón lleva su mensaje, y sirve para saber de dónde vino la persona sin
preguntárselo.

| Origen | Mensaje precargado |
|---|---|
| Genérico | `Hola PanaClaw, quiero cotizar mi sitio web` |
| Anuncio de un plan | `Hola PanaClaw, me interesa el plan Corporate` |
| Página de eBot | `Hola PanaClaw, quiero saber de eBot` |
| Página de seguridad | `Hola PanaClaw, quiero la Auditoría de Seguridad` |
| Diagnóstico | `Hola PanaClaw, quiero el Diagnóstico de Ventas` |

Sin emojis, sin exclamaciones, en primera persona del cliente.

---

## Cómo se responde

Se escribe **como escribe una persona**, no como escribe una empresa. El detalle
completo está en
[`prompts/texto/organico.md`](../../prompts/texto/organico.md).

- 1–3 líneas por mensaje
- Sin saludo protocolario, sin firma, sin «estimado cliente»
- Sin emojis
- **La cifra va pronto.** Es lo que la persona vino a preguntar

### La primera respuesta

```
[la cifra del plan que encaje] + [el plazo] + [qué incluye en una línea] +
[una pregunta concreta para saber cuál le toca]
```

> Start son $295 y sale en 72 horas: 4 o 5 secciones, los mensajes te llegan al
> WhatsApp y la publicación va incluida. ¿Necesitas también un blog o poder
> editar los textos tú mismo? Ahí ya sería Corporate, $850.

**Da la cifra antes de calificar.** La marca no retiene el precio para forzar una
conversación — eso es exactamente lo que hace la competencia y contra lo que se
posiciona.

### Cuando falta un dato

> No tengo ese dato. Lo que sí puedo decirte es X.

Nunca se rellena con una estimación.

---

## Horario

**Lun–Vie · 9:00–18:00 · hora de Panamá (GMT-5).**

Se publica. Si alguien escribe fuera de horario, se contesta cuando abre — sin
disculpas largas ni respuestas automáticas de «su mensaje es muy importante».

> Esto es, literalmente, el problema que resuelve eBot ($499): las mismas cinco
> preguntas a las once de la noche y en domingo. Si el volumen de mensajes fuera
> de horario empieza a doler, la marca tiene su propio producto para eso.

---

## Difusión: no

Nada de listas de difusión ni mensajes masivos. Tres razones:

1. Meta lo penaliza y puede costar el número
2. Es exactamente el tipo de interrupción que esta marca no hace
3. No hay una base de contactos que hayan pedido recibir nada

**Escribirle de vuelta a quien ya escribió** sí es válido, y es una de las
funciones del panel de eBot (la pantalla «Campañas»).

---

## Antes de mandar un mensaje

- [ ] ¿1–3 líneas?
- [ ] ¿La cifra está, y coincide con `datos/precios.json`?
- [ ] ¿Emojis, exclamaciones, saludo protocolario?
- [ ] ¿Dice qué no incluye, si se anunció un precio o un plazo?
- [ ] ¿Se está prometiendo algo que el catálogo no cubre?
