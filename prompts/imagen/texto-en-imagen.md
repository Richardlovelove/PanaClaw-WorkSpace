# Imagen · Texto dentro de la pieza

Cómo se maqueta una pieza de redes donde **el texto ya viene puesto**. Es la
especificación de diseño gráfico de la marca: retícula, escala, dónde cae cada
cosa y por qué.

**Antes:** [`datos/marca.json`](../../datos/marca.json) → `redesSociales`. Los
valores mandan desde ahí; este archivo explica cómo se usan.

---

## Las dos capas, y por qué no se mezclan

Una pieza de PanaClaw son **dos capas separadas**:

```
CAPA 2   El texto        Antonio y Archivo de verdad, compuesto sobre la imagen
CAPA 1   El fondo        Generado por el motor de imagen. Sin una sola letra
```

El motor genera la capa 1 y **nunca** la capa 2. No es una preferencia: los
motores de imagen siguen comiéndose las tildes y convirtiendo la eñe en ene, y
ninguno reproduce Antonio con su interlínea de 0.88. Una pieza que dice
«CODIGO TUYO» sin tilde ya no es de esta marca.

Lo que cambia respecto de como se trabajaba antes es **quién monta la capa 2**.
Antes se montaba a mano en Canva. Ahora la monta el HTML que devuelve el modelo,
con las fuentes cargadas y las medidas de este archivo escritas en el código —
y el resultado se descarga ya en 1080×1350.

> Canva deja de ser el paso obligatorio y pasa a ser el retoque:
> [`prompts/plataformas/canva.md`](../plataformas/canva.md).

---

## La retícula

Sobre lienzo de 1080×1350. Todas las medidas en píxeles.

```
0 ────────────────────────────────────────────── borde superior
                        ⌁                          96   rayo, 64×64, centrado
72 │                                          │ 1008   márgenes laterales
   │                                          │
   │  ANTETÍTULO EN NARANJA                   │        (opcional)
   │  TITULAR EN ANTONIO                      │  ← el bloque de texto se ancla
   │  QUE OCUPA VARIAS LÍNEAS                 │     arriba, al medio o abajo
   │  bajada gris de apoyo                    │
   │  $CIFRA                                  │        (si la pieza la lleva)
   │  NOTA DEL LÍMITE                         │        (obligatoria si hay cifra)
   │                                          │
   │  PANACLAW.                               │ 1254   wordmark, base del bloque
1350 ───────────────────────────────────────────── borde inferior
```

**Todo se alinea a la izquierda, en x=72.** El rayo es la única excepción: va
centrado. Es la misma composición del sitio, donde el titular cae siempre en el
carril izquierdo del contenedor.

### El orden del bloque no se negocia

De arriba abajo, siempre, sin excepción:

```
ANTETÍTULO      el tema, o el nombre del producto
TITULAR         lo que se lee de lejos
bajada          si la lleva
CIFRA           si la lleva
NOTA            el límite, si hay cifra o plazo
```

**La cifra va después del titular, nunca antes.** Un importe suelto encima del
antetítulo no tiene de qué ser el precio todavía: el lector se encuentra el
número antes que la cosa. El titular monta el argumento y la cifra lo cierra —
por eso `cifra` lleva 44 px de aire por encima y no por debajo.

Es el error que comete un modelo cuando se le da la escala pero no el orden, y
se detecta en un vistazo: si lo primero que lees en la pieza es un número, está
al revés.

### Los tres anclajes verticales

El bloque de texto no se centra a ojo. Se ancla a uno de tres sitios, y lo
decide el número de líneas del titular:

| Anclaje | Dónde | Cuándo |
|---|---|---|
| **Alto** | Tope del bloque en y=248 | Titular de 6–8 líneas |
| **Medio** | Centro óptico del bloque en y=594 | Titular de 3–5 líneas |
| **Bajo** | Base del bloque en y=1112 | La imagen manda en la mitad superior |

**594 y no 675.** El centro óptico va por encima del centro geométrico: un
bloque centrado matemáticamente se lee caído. Es el ajuste que separa una pieza
compuesta de una pieza colocada.

---

## La escala

El tamaño del titular **lo decide el número de líneas**, no el gusto de quien
maqueta. Es lo que hace que doce piezas del mismo mes se vean hermanas.

| Rol | Familia | Peso | Tamaño | Interlínea | Tracking | Color |
|---|---|---|---|---|---|---|
| Titular XL · 2–3 líneas | Antonio | 700 | 132 | 0.88 | −0.01em | `#FFF7F7` |
| Titular L · 4–5 líneas | Antonio | 700 | 112 | 0.88 | −0.01em | `#FFF7F7` |
| Titular M · 6–8 líneas | Antonio | 700 | 92 | 0.90 | −0.01em | `#FFF7F7` |
| Antetítulo | Archivo | 500 | 24 | — | 0.16em | `#FF5100` |
| Bajada | Archivo | 300 | 30 | 1.45 | — | `#BABABA` |
| Nota / límite | Archivo | 400 | 20 | 1.5 | 0.14em | `#BABABA` |
| Cifra | Antonio | 700 | 76 | — | 0 | `#FFF7F7` |
| Wordmark | Archivo | 700 | 30 | — | 0.22em | `#FFF7F7` + punto `#FF5100` |

**Titular y cifra siempre en versalitas.** La bajada nunca: en minúscula se lee
mucho más rápido, y la bajada está para leerse.

**Más de 8 líneas no es un titular, es un párrafo.** Si no cabe en ocho, el
mensaje tiene dos ideas y son dos piezas.

**El número de líneas propone, el carácter más largo dispone.** Si una línea se
pasa del rango de caracteres de su tamaño, baja un escalón. Un titular de tres
líneas donde una tiene 19 caracteres es un titular L, no XL.

### eBot no cabe en un titular

**`eBot` se escribe con e minúscula y B mayúscula, siempre.** El titular va en
versalitas, así que dentro de un titular se convertiría en `EBOT`, que es una de
las tres formas que la marca prohíbe expresamente.

La salida es una sola, y es limpia:

> **El nombre del producto vive en el antetítulo, y el antetítulo respeta su
> escritura.** El antetítulo va en versalitas *salvo* cuando contiene un nombre
> con minúscula obligatoria. Ahí se escribe tal cual: `eBot`.

```
✓  eBot                          ← antetítulo, escritura respetada
   ATIENDE TUS MENSAJES.         ← titular en versalitas, sin el nombre dentro
   NO REEMPLAZA TU SITIO.

✗  EBOT ATIENDE TUS MENSAJES.    ← el nombre roto dentro del titular
```

En la descripción no hay problema: va en caja normal y se escribe `eBot`.

Aplica a cualquier nombre futuro que lleve minúscula obligatoria, no solo a este.

### Antonio a −0.01em, no a −0.02em

El titular del sitio va a −0.02em porque Archivo es de ancho normal y necesita
cerrarse. Antonio ya viene condensada; a −0.02em las letras se tocan y la
palabra deja de leerse a tamaño de pulgar.

---

## El acento naranja

Es la decisión que más define la pieza y la que más fácil se arruina.

**Un solo tramo del titular va en `#FF5100`. Continuo. Nunca más de la mitad de
los caracteres.** Todo lo demás en `#FFF7F7`.

> El tope estuvo un rato en el 40 % y estaba mal. La pieza publicada que mejor
> funciona —«no hacemos cubos con brasa / hacemos obsidiana fría, rápida»— lleva
> el 56 % en naranja, porque la afirmación es más larga que la negación y eso es
> exactamente lo que la hace funcionar. **Lo que rompe una pieza no es la
> proporción: es que haya dos tramos naranjas en vez de uno.**

```
✓  NO HACEMOS PLANTILLAS.
   CADA SITIO ES CÓDIGO NUEVO.        ← «código nuevo» en naranja

✗  NO HACEMOS PLANTILLAS.             ← dos tramos naranjas: ya no hay acento,
   CADA SITIO ES CÓDIGO NUEVO.           hay dos colores peleando
```

**Qué va en naranja:** la afirmación, la consecuencia o la cifra. En un titular
con forma «no hacemos X, hacemos Y», el naranja es **Y**.

**Qué no va nunca en naranja:** la negación, la bajada, la nota, ni el titular
entero. Un titular entero en naranja no tiene acento — es una pieza naranja.

**`#FF1E1E` no toca una letra.** Aquí tampoco. Es color de fondo, y en cuanto
aparece en un texto hay dos rojos discutiendo cuál es el acento de la marca.

---

## Los cortes de línea se escriben, no se calculan

Ninguna línea de titular la parte el navegador. Se decide dónde corta, y corta
**por unidad de sentido**.

```
✓  NO HACEMOS
   SIMETRÍA BONITA
   PERO LENTA.

✗  NO HACEMOS SIMETRÍA          ← «simetría bonita» partido por la mitad:
   BONITA PERO LENTA.              se lee en dos tiempos y pierde el golpe
```

Tres reglas:

1. **Una unidad de sentido por línea.** Sujeto, o verbo con su objeto, o el
   remate. No se parte un sustantivo de su adjetivo.
2. **Sin líneas huérfanas**, salvo que la huérfana sea el remate. `PERO LENTA.`
   sola es buena; `NUEVO.` sola es buena; una preposición sola nunca.
3. **La última línea lleva el punto.** El titular de esta marca termina. Es la
   voz: frases que terminan.

---

## El velo

La imagen va a sangre y **bajo un velo que abre el carril del texto**. Es la
regla 9 del sitio, con los números recalculados: allí la imagen es el fondo de
una sección larga y va al 0.4–0.5; aquí la imagen es el 100 % de la pieza, y a
ese valor se ve un rectángulo negro con una mancha.

- **Brillo de la imagen:** 0.55–0.75
- **Degradado:** lineal, desde el borde donde cae el texto hacia el opuesto.
  De `rgba(16,1,1,0.92)` a `rgba(16,1,1,0.10)`

**Ninguna caja detrás del texto.** Ni tarjeta, ni franja, ni rectángulo
semitransparente, ni sombra sobre las letras. El contraste lo pone el velo, que
es continuo y no tiene borde. Una caja detrás de un titular es la señal más
rápida de que la pieza se maquetó sin sistema.

Si con el velo puesto el titular todavía compite con la imagen, **el fondo está
mal generado**: se regenera pidiendo que la incandescencia se apague antes de
llegar al carril. No se sube el velo hasta tapar la imagen.

---

## El rayo y el wordmark

**Símbolo:** 88 de ancho por 72 de alto, centrado horizontalmente, borde superior
en y=96. Es la garra de tres zarpazos sobre los corchetes angulares. El path
completo sale de [`datos/marca.json`](../../datos/marca.json) → `logo.pathSVG`,
en `viewBox="0 0 100 81.56"` y con `fill-rule="evenodd"`. El archivo está en
[`logo-original.svg`](../../logo-original.svg).

Tres cosas que se rompen solas si no se dicen:

1. **No es cuadrado.** 100 × 81.56. Meterlo en una caja cuadrada lo estira, y
   estirar el símbolo está en la lista de usos prohibidos.
2. **`fill-rule="evenodd"`.** Sin eso los huecos de los corchetes se rellenan y
   el logo sale como una mancha.
3. **Naranja `#FF5100` plano**, sin degradado. A 88 píxeles el degradado a ember
   no se ve y solo ensucia el borde.

Sobre fondo oscuro no lleva cuadrado detrás: el fondo ya es el cuadrado.

**Wordmark:** `PANACLAW` en Archivo 700, tracking 0.22em, `#FFF7F7`, **seguido de
un punto en `#FF5100`**. Alineado a la izquierda en x=72, base del bloque en
y=1254.

> **Divergencia detectada.** Las piezas que la marca ha publicado hasta ahora
> parten el wordmark en dos colores —`PANA` blanco y `CLAW` naranja, sin punto—
> y eso no es lo que declara `marca.json` ni lo que usa el sitio. Aquí manda el
> JSON. Si la versión partida va a ser la oficial, se cambia primero en el sitio
> y después baja aquí, como todo: [`operacion/sincronizacion.md`](../../operacion/sincronizacion.md).

---

## Carrusel

- **Todas las diapositivas 1080×1350.** Mezclar proporciones deja bandas al
  deslizar.
- **El anclaje del texto no salta.** Si la primera va anclada al medio, las
  demás también. El deslizamiento tiene que sentirse como una sola pieza larga,
  no como cinco piezas distintas seguidas.
- **El rayo y el wordmark van en todas.** Cada diapositiva se puede compartir
  suelta.
- **La primera lleva el peso.** Es la única que se ve en el feed sin deslizar:
  el titular más corto y más grande del carrusel va ahí.
- **La última cierra o pide algo.** No se deja morir en un dato.
- **Numerador:** apagado por defecto. Si se enciende, va en la esquina superior
  derecha en x=1008, formato `01/05`, en `#BABABA`.

---

## Antes de dar una pieza por buena

- [ ] ¿El titular es Antonio 700 en versalitas, y el resto Archivo?
- [ ] ¿El tamaño corresponde al número de líneas, y ninguna línea se pasa de su
      rango de caracteres?
- [ ] ¿Algún nombre de minúscula obligatoria —`eBot`— metido dentro del titular?
- [ ] ¿Hay **un solo** tramo naranja, y es la afirmación o la cifra?
- [ ] ¿Alguna letra en `#FF1E1E`?
- [ ] ¿Los cortes de línea respetan las unidades de sentido?
- [ ] ¿Alguna línea huérfana que no sea el remate?
- [ ] ¿Alguna caja, franja o sombra detrás del texto?
- [ ] ¿El wordmark lleva su punto naranja?
- [ ] ¿Todo alineado a x=72, con el rayo como única excepción centrada?
- [ ] ¿Se lee el titular al tamaño de un pulgar? Aléjate y míralo pequeño.
- [ ] Si la pieza dice una cifra, ¿está la nota del límite debajo?
- [ ] **Mira la banda del símbolo, y 96 a 168.** ¿Asoma algo del fondo detrás?
      Si hay resplandor, forma o reflejo, el fondo está mal generado y se
      regenera. El símbolo naranja sobre un resplandor naranja desaparece.
- [ ] Lo mismo en la banda del wordmark, de y 1190 a 1350.
- [ ] ¿El wordmark termina en y=1254? Si se colocó por su borde superior en vez
      de por su base, queda unos 14 px alto y se nota contra el margen.

### La comprobación que no se puede saltar

**Descarga la pieza y ponla al lado de su vista previa.** Si no son idénticas, el
exportador está mal — y si está mal en una, está mal en todas. Las cinco trampas
que lo causan están en
[`prompts/plataformas/meta-ai.md`](../plataformas/meta-ai.md).

Un desfase de dos o tres píxeles entre las dos es normal y viene de que el lienzo
posiciona por la caja del tipo y el navegador por la caja de línea. Por encima de
seis, algo está mal calculado.
