# Plantilla · Estructura de anuncio

Una pieza de pauta, campo a campo. **Se rellena, no se copia**: aquí no hay copy
escrito.

Cómo se escribe el texto:
[`prompts/texto/anuncios.md`](../../prompts/texto/anuncios.md).

**Y con qué oficio se llena cada hueco:**
[`adn/06-claridad.md`](../../adn/06-claridad.md) —qué se dice primero y con qué
palabras— y [`adn/07-redaccion.md`](../../adn/07-redaccion.md) —las palancas, la
prueba, el gancho y el ritmo—. Esta plantilla dice qué va en cada campo; esos dos
dicen cómo se escribe para que funcione.

---

## La ficha

```
CAMPAÑA
  Público            uno de los seis de adn/04-audiencia.md
  Etapa              frío · tibio · decisión
  Producto           del catálogo
  Precio             verificado contra datos/precios.json
  Ángulo             precio · propiedad · plazo · velocidad   (UNO)
  Hipótesis          qué se está probando con esta pieza

TEXTO
  Gancho             la situación, 2ª persona, presente. Sin nombrar la marca
  Giro               por qué le pasa, o qué se hace distinto
  Cifra              el precio o el plazo, desnudo
  Límite             qué no incluye, o desde cuándo cuenta el plazo
  CTA                una sola acción

VISUAL
  Escena             de las siete madre (prompts/README.md)
  Proporción         1:1 · 4:5 · 9:16 · 1.91:1
  Texto en imagen    sí / no  (por defecto: no)

DESTINO
  URL                /planes/ · /cotizador/ · /ebot/ · /seguridad/ · WhatsApp
  Métrica            qué evento cuenta como éxito
```

---

## Los cuatro campos de texto

### Gancho

La situación del que mira, **en segunda persona y en presente**. Sin nombrar la
marca, sin pregunta retórica.

```
✗  ¿Cansado de que tu web sea lenta?
✗  En PanaClaw hacemos webs rápidas
✓  Tu web tarda y la gente se va antes de ver lo que vendes
```

Sale de la columna «situación» de
[`adn/04-audiencia.md`](../../adn/04-audiencia.md).

### Giro

Por qué le pasa eso de verdad, o qué se hace distinto. Es lo que separa un
anuncio de un eslogan.

```
✓  Pasa porque cada proyecto se empieza desde cero. El nuestro no.
✓  Casi siempre es lo mismo: un complemento sin actualizar.
```

### Cifra

Sola, sin adornar, sin «solo», sin «desde tan solo».

```
✗  ¡Desde solo $295!
✓  $295. Lista en 72 horas.
```

### Límite

**El campo que casi nadie pone y el que hace que esta marca suene distinta.**

```
✓  El reloj arranca cuando nos das tus textos y la mitad del pago.
✓  Los $5 de la nube y el gasto de la IA se pagan aparte, no a nosotros.
✓  La auditoría se paga siempre y va antes que cualquier plan mensual.
```

No es letra pequeña: va en el cuerpo del anuncio, con el mismo peso que la cifra.

---

## Límites por canal

| Canal | Formato | Titular | Cuerpo | Notas |
|---|---|---|---|---|
| Meta feed | 4:5 · 1080×1350 | ~40 car. | ~125 car. antes de «ver más» | El gancho tiene que caber ahí |
| Meta story | 9:16 · 1080×1920 | ~30 car. | mínimo | Zonas seguras: 15 % arriba, 20 % abajo |
| Meta reel | 9:16 · 1080×1920 | — | — | Ver `prompts/video/video-corto.md` |
| Google Search | texto | 3 × 30 car. | 2 × 90 car. | Ver `canales/google.md` |
| Google Display | 1.91:1 · 1200×628 | ~30 car. | ~90 car. | Texto a la izquierda |

**Las primeras 125 caracteres de Meta son el anuncio entero.** El gancho y la
cifra tienen que estar ahí; el giro y el límite pueden caer después del «ver
más».

---

## El grupo de variantes

Cuando se pidan varias, **una hipótesis por variante**:

| | Ángulo | Gancho sobre |
|---|---|---|
| A | Velocidad | Su sitio tarda y pierde gente |
| B | Propiedad | Depende de su agencia y no puede irse |
| C | Plazo | Lleva meses esperando |
| D | Precio publicado | Nadie le da una cifra |

**Todo lo demás se mantiene igual** entre variantes: misma imagen, mismo
producto, mismo destino. Si cambian dos cosas, la prueba no dice nada.

---

## Antes de publicar

- [ ] ¿Los cuatro campos de texto, incluido el límite?
- [ ] ¿El gancho es una situación, en 2ª persona y en presente?
- [ ] ¿La cifra coincide con `datos/precios.json`?
- [ ] ¿Los rangos van enteros o con «desde»?
- [ ] ¿Algún pago único sumado a una mensualidad?
- [ ] ¿Una sola llamada a la acción?
- [ ] ¿El CTA de WhatsApp va sin número?
- [ ] ¿Emojis, exclamaciones, urgencia o descuentos inventados?
- [ ] ¿Alguna métrica o testimonio que no exista?
- [ ] ¿El texto cabe en los primeros 125 caracteres de Meta?
- [ ] ¿La imagen tiene el hueco limpio donde cae el titular?
