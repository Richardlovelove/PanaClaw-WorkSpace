# Plataforma · Canva

Canva es donde se **retoca**, no donde se genera el estilo ni donde se maqueta el
mes. El sistema visual de PanaClaw es demasiado específico para que su IA lo
deduzca; lo que sí hace bien es ajustar a mano una pieza concreta.

> **Canva dejó de ser el paso obligatorio.** El lote de redes se compone solo,
> con las fuentes reales y la retícula en píxeles, en el documento HTML que
> devuelve Meta AI: [`meta-ai.md`](meta-ai.md) y
> [`prompts/imagen/texto-en-imagen.md`](../imagen/texto-en-imagen.md). Maquetar a
> mano doce piezas es doce oportunidades de que el tracking salga distinto.

**Cuándo sigue siendo Canva:** una pieza suelta, un retoque sobre algo ya
compuesto, una adaptación a otra proporción, o cualquier cosa que no sea el lote
del mes.

**Flujo:** la imagen se genera en Nano Banana → se maqueta en Canva con la escala
de [`prompts/imagen/texto-en-imagen.md`](../imagen/texto-en-imagen.md).

---

## Configurar el Brand Kit

Una vez, y todo lo demás sale bien solo.

### Colores

```
#100101   Fondo
#FF5100   Acento
#FF1E1E   Solo fondos
#FFF7F7   Texto
#BABABA   Texto secundario
```

**Cinco. Ni uno más.** Si el kit tiene un sexto color, alguien lo va a usar.

### Fuentes

**Dos, y solo dos.** Las dos están en Google Fonts, así que Canva las tiene.

| Rol | Fuente | Peso | Ajustes |
|---|---|---|---|
| Titular | **Antonio** | 700 | Versalitas, tracking −1 %, interlínea 0.88 |
| Cifra | **Antonio** | 700 | Versalitas, tracking 0 |
| Antetítulo | Archivo | 500 | Versalitas, tracking +16 %, color `#FF5100` |
| Bajada | Archivo | 300 | Interlínea 1.45, color `#BABABA` |
| Nota / límite | Archivo | 400 | Versalitas, tracking +14 %, color `#BABABA` |
| Wordmark | Archivo | 700 | Versalitas, tracking +22 %, punto en `#FF5100` |

Los tamaños en píxeles sobre lienzo de 1080×1350 están en
[`prompts/imagen/texto-en-imagen.md`](../imagen/texto-en-imagen.md). **Para
piezas de web y anuncios, el titular sigue siendo Archivo 600 a −2 %** — Antonio
es solo de redes.

> Canva no tiene «tracking negativo» con ese nombre: es **Espaciado entre
> letras**, en valor negativo. Es el ajuste que más se olvida y el que más se
> nota: sin él, el titular deja de parecer de esta marca.

### Logo

Sube el `favicon.svg` del sitio (rayo naranja) y el wordmark. **Solo versión
sobre fondo oscuro** — no subas variantes sobre claro, porque no existen.

---

## Plantillas a crear

Cinco maestras cubren casi todo. Cada una con la imagen como fondo a sangre y el
texto encima.

| Plantilla | Medida | Composición |
|---|---|---|
| Feed cuadrado | 1080 × 1080 | Antetítulo + titular + cifra, tercio inferior |
| Feed vertical | 1080 × 1350 | Igual, más aire |
| Story | 1080 × 1920 | Bloque de texto centrado-bajo, zonas seguras libres |
| Anuncio horizontal | 1200 × 628 | Texto en la mitad izquierda |
| Ficha de precio | 1080 × 1350 | Cifra grande + qué incluye + qué no incluye |

**La quinta es la más útil y la que nadie más tiene.** Es la pieza firma de la
marca: el precio, lo que incluye y **lo que no**, en el mismo creativo.

---

## Anatomía de una pieza

De arriba abajo:

```
ANTETÍTULO        14 px equivalente, versalitas, tracking +16%, #FF5100
TITULAR           Versalitas, peso 600, tracking −2%, #FFF7F7, máx. 14 caracteres/línea
BAJADA            Peso 300, #BABABA, máx. 52 caracteres de ancho
[espacio]
CIFRA             Peso 600, grande. Sola.
LÍMITE            Peso 300, #BABABA, pequeño. "Qué no incluye" o "desde cuándo cuenta el plazo".
```

El bloque «límite» es opcional en el layout pero **obligatorio en el contenido**
cuando la pieza anuncia un precio o un plazo.

---

## Reglas de maquetación

- **La imagen va a sangre**, siempre. Nunca con marco, ni con margen blanco, ni
  dentro de una forma.
- **El texto va sobre negro limpio**, no sobre el sujeto. Si no hay hueco, la
  imagen está mal generada — vuelve a Nano Banana en vez de meter una caja
  semitransparente detrás del texto.
- **Ninguna caja de color detrás del texto.** El contraste lo pone el negro de la
  imagen.
- **Viñetas: punto naranja.** Nunca check verde, nunca guion, nunca icono.
- **Botones y etiquetas: píldora completa** (radio máximo). Tarjetas: 20 px.
- **Nunca texto en `#FF1E1E`.** El ember es color de fondo.

---

## Qué NO usar de Canva

La biblioteca de Canva está llena de cosas que rompen este sistema en un clic:

- **Fotos de stock.** Ninguna encaja: todas tienen luz natural, personas u
  oficinas.
- **Ilustraciones y elementos gráficos.** Iconos, formas, adornos, «doodles».
- **Degradados de la biblioteca.** Los de la marca son negro → naranja/ember y se
  hacen a mano.
- **Animaciones de texto.** Rebotes, máquinas de escribir, deslizamientos. El
  movimiento de la marca es solo opacidad.
- **Plantillas prediseñadas.** Todas traen su propio sistema y hay que
  desmontarlo entero; sale más rápido partir de un lienzo vacío.

---

## La IA de Canva (Magic Studio)

**Para generar imágenes: no.** No reproduce este sistema visual y no acepta
control de hex. Genera en Nano Banana y sube el archivo.

**Para redimensionar (Magic Resize): sí, con revisión.** Adaptar una pieza
aprobada a otras proporciones es donde más tiempo ahorra. Después de cada
redimensión, comprueba:

- [ ] ¿El titular sigue cayendo sobre negro limpio?
- [ ] ¿Se partió el sujeto de la imagen?
- [ ] ¿El texto quedó fuera de las zonas seguras de story?

**Para escribir copy: no.** Pega el texto ya escrito contra este repositorio.

---

## Antes de exportar

- [ ] ¿Antonio en el titular y la cifra, Archivo en todo lo demás?
- [ ] ¿El tracking correcto en cada rol?
- [ ] ¿Algún color fuera de los cinco?
- [ ] ¿Algún texto en `#FF1E1E`?
- [ ] ¿La cifra coincide con `datos/precios.json`?
- [ ] ¿Está el «qué no incluye» si la pieza anuncia precio o plazo?
- [ ] ¿Se coló un elemento de la biblioteca de Canva?
- [ ] ¿La imagen va a sangre, sin marco?
