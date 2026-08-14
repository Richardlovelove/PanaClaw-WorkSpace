# Texto · Anuncios

Estructura de copy para pauta. La plantilla completa de una pieza de anuncio,
con sus campos por canal, está en
[`campanas/plantillas/estructura-anuncio.md`](../../campanas/plantillas/estructura-anuncio.md).
Esto es cómo se **escribe** el texto.

---

## La estructura de cuatro partes

```
1. GANCHO      La situación del que mira. Sin nombrar la marca.
2. GIRO        Por qué le pasa eso, o qué se hace distinto.
3. CIFRA       El precio o el plazo. Desnudo.
4. LÍMITE      Qué no incluye, o desde cuándo cuenta el plazo.
```

Las cuatro. El cuarto es el que la mayoría de los anuncios se salta y el que hace
que este suene distinto.

### Ejemplo de la forma

```
1  Preguntaste por una web y te dijeron "un mes y medio". Van tres.
2  Pasa porque cada proyecto se empieza desde cero. El nuestro no.
3  $295. Lista en 72 horas.
4  El reloj arranca cuando nos das tus textos y la mitad del pago.
```

No es un anuncio de catálogo para copiar: es la forma. El copy se escribe cada
vez, contra el contexto.

---

## El gancho: dónde sale

El gancho no se inventa. Sale de la columna «situación» de
[`adn/04-audiencia.md`](../../adn/04-audiencia.md):

| Público | Gancho, en bruto |
|---|---|
| No tiene sitio | Manda a sus clientes a un perfil de Instagram |
| WordPress que da vergüenza | Se le cayó una vez y nadie supo por qué |
| Invierte en publicidad | Paga clics que caen en una página lenta |
| Quiere vender en línea | Apunta pedidos a mano y pierde la cuenta del stock |
| No da abasto con mensajes | Las mismas cinco preguntas, a las once de la noche |
| No sabe si está expuesto | Oyó de alguien a quien le tumbaron la web |

**Escríbelo en segunda persona y en presente.** «Se te acumulan los mensajes sin
contestar», no «¿Se te acumulan los mensajes?». La marca afirma, no pregunta.

---

## La cifra: cómo se pone

Sola, en su línea, sin adornar.

```
✗  ¡Desde solo $295!
✗  Sitios web a partir de $295 USD
✗  Precios desde $295 (consulta condiciones)
✓  $295. Lista en 72 horas.
```

**Verifica contra [`datos/precios.json`](../../datos/precios.json)** en el momento
de escribirla, no de memoria. Y si es un rango, entero: `$80–$150` o
`desde $80`, nunca `$80` a secas.

---

## Por etapa del embudo

### Frío — no conoce la marca

- **Ataca la situación**, no la objeción. Todavía no tiene ninguna.
- El gancho es todo. Si la primera línea no lo reconoce, no hay segunda.
- La cifra va pronto: es el diferenciador de categoría de esta marca.
- **Producto recomendado:** Diagnóstico de Ventas ($49) o Start ($295). Son las
  dos cifras lo bastante bajas para decidirse en un anuncio.

### Tibio — visitó y no escribió

- **Ataca la objeción principal** de ese público. Está catalogada en
  [`adn/04-audiencia.md`](../../adn/04-audiencia.md).
- Esta persona ya vio el precio. Repetírselo no añade nada; lo que la frena está
  en otro sitio.

### Remarketing — llegó al cotizador o al formulario y no envió

- **Una sola frase, y es una promesa de propiedad o de límite.** «El código queda
  a tu nombre.» «Cada plan trae sus rondas de cambios; la extra cuesta $40 y se
  sabe de antemano.»
- Nada de urgencia, descuentos ni cuenta atrás. No existen, y fabricarlos
  contradice el argumento completo.

---

## Variantes para probar

Cuando pidan «cuatro variantes», que cada una pruebe **una hipótesis distinta**,
no cuatro redacciones del mismo mensaje.

| Variante | Hipótesis |
|---|---|
| A | Gancho por **velocidad** — le duele que su sitio sea lento |
| B | Gancho por **propiedad** — le duele depender de su agencia |
| C | Gancho por **plazo** — le duele la espera |
| D | Gancho por **precio publicado** — le duele que nadie le dé una cifra |

Cuatro redacciones de «tu web en 72 horas» no son cuatro variantes: son una, con
ruido.

---

## Prohibido en anuncios

Además de todo lo de [`adn/02-voz-y-tono.md`](../../adn/02-voz-y-tono.md):

- **Urgencia falsa.** «Oferta por tiempo limitado», «últimos cupos», cuenta atrás.
  No existen y son lo contrario de un precio publicado que no cambia.
- **Descuentos.** El único del catálogo es Care anual = dos meses gratis.
- **Interrogaciones de teletienda.** «¿Cansado de tu web lenta?» La marca afirma.
- **Emojis.** Ninguno, tampoco en pauta.
- **Prometer Google.** Ni posiciones, ni plazos, ni visitas.
- **Testimonios o métricas.** No hay verificados. Ver
  [`catalogo/09-prueba.md`](../../catalogo/09-prueba.md).

---

## El destino del clic

Se decide antes de escribir, porque cambia el CTA:

| Destino | Cuándo | CTA |
|---|---|---|
| `/planes/` | Frío, sabe lo que quiere | «Mira los cuatro planes» |
| `/cotizador/` | Tibio, no sabe cuál le toca | «Calcula el tuyo» |
| `/ebot/` · `/seguridad/` | Anuncio de ese producto | «Cómo funciona» |
| WhatsApp | Tibio o remarketing, quiere hablar | «Escríbenos por WhatsApp» |

**El CTA de WhatsApp nunca lleva el número.** Dice «WhatsApp» y el enlace se
compone con la plantilla de
[`datos/marca.json`](../../datos/marca.json) → `contacto.plantillaEnlace`.

---

## Antes de entregar

- [ ] ¿Están las cuatro partes, incluido el límite?
- [ ] ¿El gancho es una situación en segunda persona y en presente?
- [ ] ¿La cifra coincide con `precios.json`?
- [ ] ¿Los rangos van enteros?
- [ ] ¿Hay algún importe único sumado a uno mensual?
- [ ] ¿Un emoji, una exclamación, una urgencia inventada?
- [ ] ¿Cada variante prueba una hipótesis distinta?
- [ ] ¿Una sola llamada a la acción?
