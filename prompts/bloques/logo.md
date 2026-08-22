# Bloque · El logo

**El símbolo de PanaClaw no se describe, no se aproxima y no se genera: se pega.**

Este archivo es el único sitio del repositorio donde el trazado está escrito
entero y listo para copiar. Todos los demás archivos apuntan aquí. Existe porque
describir el logo en vez de entregarlo ya costó un lote completo.

---

## Lo que pasó el 2026-08-22

Se le pasó a Meta AI el prompt maestro de un carrusel. El documento volvió bien
—retícula exacta, tildes respetadas, texto literal, costuras limpias— con el
logo inventado en las cinco diapositivas.

Dibujó esto, en la vista previa y otra vez en el lienzo de exportación:

```
tres trazos diagonales paralelos, stroke #FFF7F7, grosor 8, extremos
redondeados, dentro de un viewBox 0 0 88 72
```

Cuatro cosas mal a la vez: el trazado es inventado, el color es blanco en vez de
naranja, son líneas con grosor en vez de figuras rellenas, y faltan tres de las
seis figuras del símbolo —los dos corchetes y el punto romboidal.

**No fue desobediencia.** El prompt le daba la caja del símbolo —88 × 72,
esquina superior en y=96— y la descripción en palabras —«la garra de tres
zarpazos sobre los corchetes angulares»—, y para el trazado le decía que saliera
de `datos/marca.json`, que es un archivo al que Meta AI no tiene acceso. Recibió
un hueco con medidas y una descripción, y lo rellenó. Cualquier modelo lo habría
rellenado.

De ahí sale la regla: **un prompt que nombra el logo lleva el logo dentro.** Un
puntero a este repositorio no es entregar el logo.

---

## El símbolo, para pegar en HTML

Va literal, sin tocar una coma. Es lo que se pone en el documento del mes, en
una landing, en un correo o en cualquier pieza que se componga en el navegador:

```html
<svg width="88" height="72" viewBox="0 0 100 81.56" aria-hidden="true">
  <path fill="#FF5100" fill-rule="evenodd" d="M73.43 28.64L54.69 50.19L42.73 77.94L67.38 50.63L67.45 47.83L68.19 44.36Z M81.03 21.85L73.95 28.93L85.68 40.52L67.9 58.38L75.2 65.76L100 40.52Z M74.61 15.5L74.39 15.5L73.8 16.09L73.65 16.39L73.28 16.61L72.69 17.2L72.62 17.42L67.6 22.44L67.6 22.59L72.1 27.01L72.25 27.01L79.19 20.08Z M25.17 15.35L0 40.3L25.39 65.32L32.32 58.16L14.32 40.37L32.18 22.36Z M59.26 1.77L32.69 28.79L32.62 31.52L31.59 36.31L26.64 51.74L45.68 29.75L50.41 19.41Z M75.94 0.15L52.18 27.24L50.85 31L41.62 43.62L23.91 81.56L48.12 52.55L49.89 47.98L59.04 35.65Z"/>
</svg>
```

El `viewBox`, el `fill-rule` y el `d` no se tocan nunca. Para otro tamaño se
cambia `width`, y `height` con él.

**En SVG el símbolo no se puede estirar por accidente.** `preserveAspectRatio`
vale `xMidYMid meet` por defecto: el trazado se ajusta dentro de la caja
conservando su proporción y se centra, así que un `height` de más solo deja aire
arriba y abajo. Con `width="88"` la tinta mide 88 × 71.77 en cualquier caso, y el
`height="72"` de la retícula le deja 0.23 px de holgura.

Lo único que sí lo estira es `preserveAspectRatio="none"`. **No se pone nunca.**

| Ancho de la caja | Alto de la caja | Tinta real |
|---|---|---|
| 88 | 72 | 88 × 71.77 |
| 120 | 98 | 120 × 97.87 |
| 200 | 164 | 200 × 163.12 |

---

## El símbolo, para el lienzo de exportación

Cuando la pieza se baja en PNG, el símbolo se dibuja otra vez sobre el
`<canvas>`. Es el segundo sitio donde se inventa, porque suele escribirse aparte
del maquetado:

```js
const SIMBOLO = new Path2D("M73.43 28.64L54.69 50.19L42.73 77.94L67.38 50.63L67.45 47.83L68.19 44.36Z M81.03 21.85L73.95 28.93L85.68 40.52L67.9 58.38L75.2 65.76L100 40.52Z M74.61 15.5L74.39 15.5L73.8 16.09L73.65 16.39L73.28 16.61L72.69 17.2L72.62 17.42L67.6 22.44L67.6 22.59L72.1 27.01L72.25 27.01L79.19 20.08Z M25.17 15.35L0 40.3L25.39 65.32L32.32 58.16L14.32 40.37L32.18 22.36Z M59.26 1.77L32.69 28.79L32.62 31.52L31.59 36.31L26.64 51.74L45.68 29.75L50.41 19.41Z M75.94 0.15L52.18 27.24L50.85 31L41.62 43.62L23.91 81.56L48.12 52.55L49.89 47.98L59.04 35.65Z");

// x, y = esquina superior izquierda de la caja. ancho = 88 en una pieza 1080×1350.
function dibujarSimbolo(ctx, x, y, ancho) {
  const k = ancho / 100;          // escala única: no se estira en un solo eje
  ctx.save();
  ctx.translate(x, y);
  ctx.scale(k, k);
  ctx.fillStyle = "#FF5100";
  ctx.fill(SIMBOLO, "evenodd");   // sin evenodd los corchetes se rellenan
  ctx.restore();
}
```

**`ctx.scale(k, k)` con el mismo número en los dos ejes.** Aquí es donde el
símbolo sí se estira de verdad: el lienzo no tiene `preserveAspectRatio` que lo
proteja, así que escalar 88/100 en x y 72/81.56 en y —dos números distintos— lo
deforma un 0.3 %. No se ve a simple vista y está en la lista de usos prohibidos
igual.

Con `ancho = 88` la tinta mide **88 × 71.77**. El «72» de la retícula es la caja
reservada, no la tinta: sobran 0.23 px que en el lienzo van arriba si quieres
que coincida exactamente con la vista previa, y que a esta escala no se ven.

---

## Las cinco formas de romperlo

Las cinco se han visto, y ninguna se nota si no se mira a propósito:

1. **Dibujarlo.** Trazos, líneas, garras improvisadas, una `M` estilizada,
   corchetes de texto `</>`. Cualquier cosa que no sea este `d` exacto.
2. **Sin `fill-rule="evenodd"`.** Los huecos de los corchetes se rellenan y el
   símbolo sale como una mancha sólida con forma de nada.
3. **Con `stroke` en vez de `fill`.** Son seis figuras rellenas, no seis líneas.
   Un `stroke` sobre este mismo trazado tampoco vale.
4. **En otro color.** Es `#FF5100` plano. Ni blanco, ni degradado a `#FF1E1E`
   —que por debajo de unos 200 px no se ve y solo ensucia el borde—, ni el color
   del texto de al lado.
5. **En una caja cuadrada, o con `preserveAspectRatio="none"`.** No es cuadrado:
   100 × 81.56. En SVG la proporción se conserva sola salvo que se desactive a
   propósito; en un `<canvas>` no hay red y hay que escalar igual los dos ejes.

Y una sexta que no es del símbolo sino de su sitio: **sobre fondo oscuro no
lleva cuadrado detrás.** El fondo ya es el cuadrado.

---

## El wordmark

`PANACLAW` en Archivo 700, tracking 0.22em, `#FFF7F7`, **seguido de un punto en
`#FF5100`**. El punto naranja no es decoración: es parte de la marca y es lo
primero que se cae cuando alguien recompone el wordmark de memoria.

```html
<span style="font-family:Archivo;font-weight:700;letter-spacing:0.22em;color:#FFF7F7;text-transform:uppercase">PANACLAW<span style="color:#FF5100">.</span></span>
```

No se parte en dos colores, no se escribe en Antonio y no va sin tracking.

---

## La frase que va en todo prompt que nombre el logo

Se pega literal, en el mismo bloque que el SVG de arriba:

```
El logo de PanaClaw NO se dibuja, no se aproxima y no se rediseña. El trazado
está escrito completo más abajo y es lo único que se puede usar: cópialo
carácter por carácter, con su viewBox, su fill-rule="evenodd" y su color
#FF5100. Si te falta el trazado, deja el hueco vacío y dilo — no lo rellenes
con una versión tuya. Lo mismo en el lienzo de exportación: el símbolo del PNG
es este mismo trazado, no un dibujo equivalente.
```

**Va donde va el SVG, no en otra sección.** Una prohibición separada del
trazado que la resuelve se olvida en un prompt largo, que es exactamente lo que
pasó.

---

## Verificación

Antes de entregar cualquier prompt o pieza que lleve el símbolo:

- [ ] ¿Está el `d` completo dentro del prompt, y no un enlace a este repositorio?
- [ ] ¿Es idéntico al de [`datos/marca.json`](../../datos/marca.json) → `logo.pathSVG`?
      Se compara, no se recuerda
- [ ] ¿Lleva `fill-rule="evenodd"`?
- [ ] ¿`fill="#FF5100"`, y ningún `stroke`?
- [ ] ¿Está sin `preserveAspectRatio="none"`, y en el lienzo con la misma escala
      en los dos ejes?
- [ ] Si la pieza se exporta a PNG, ¿el lienzo dibuja este mismo trazado?
- [ ] ¿Va la frase de arriba pegada al SVG, en el mismo bloque?

Y cuando vuelva la pieza: **amplía el símbolo al 400 % y cuenta las figuras.**
Tienen que ser seis —dos corchetes, un punto romboidal y tres zarpazos— y los
huecos de los corchetes tienen que verse abiertos. Tres trazos sueltos no es el
logo.

---

## De dónde sale

| Qué | Dónde |
|---|---|
| El trazado, como dato | [`datos/marca.json`](../../datos/marca.json) → `logo.pathSVG` |
| El archivo vectorial | [`logo-original.svg`](../../logo-original.svg) |
| El original rasterizado | [`logo-original.png`](../../logo-original.png) |
| Qué significa y qué está prohibido | [`adn/03-sistema-visual.md`](../../adn/03-sistema-visual.md) § Logo |
| Dónde cae en una pieza de redes | [`prompts/imagen/texto-en-imagen.md`](../imagen/texto-en-imagen.md) |

> **El favicon del sitio todavía dibuja el símbolo viejo.** Es una divergencia
> abierta con `abrinay1997-stack/PanaClaw`, anotada en
> [`operacion/deuda-conocida.md`](../../operacion/deuda-conocida.md). No lo uses
> como fuente: aquí manda `logo-original.svg`.
