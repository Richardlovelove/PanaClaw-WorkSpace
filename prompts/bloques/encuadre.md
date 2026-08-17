# Bloque · Encuadre

Proporción por canal y, sobre todo, **dónde dejar el hueco para el texto**.

El titular de PanaClaw no se genera nunca: se compone encima. Lo que se le pide
al generador es que **deje el carril limpio**.

---

## Proporciones por canal

| Canal | Proporción | Píxeles | Dónde va el texto |
|---|---|---|---|
| Instagram feed cuadrado | 1:1 | 1080 × 1080 | Tercio inferior |
| Instagram feed vertical | 4:5 | 1080 × 1350 | Tercio inferior |
| Story / Reel portada | 9:16 | 1080 × 1920 | Franja central-baja, sobre el 60 % |
| Anuncio Meta feed | 4:5 | 1080 × 1350 | Tercio inferior |
| Anuncio Meta story | 9:16 | 1080 × 1920 | Centro, evitando los bordes |
| Google Display | 1.91:1 | 1200 × 628 | Mitad izquierda |
| OpenGraph / compartir | 1.91:1 | 1200 × 630 | Mitad izquierda |
| Cabecera web (hero) | 16:9 | 1920 × 1080 | Mitad izquierda |
| LinkedIn | 1.91:1 | 1200 × 627 | Mitad izquierda |

**La regla:** vertical → texto abajo. Horizontal → texto a la izquierda. Es la
misma composición que usa el sitio, donde el titular siempre cae en el carril
izquierdo del contenedor.

---

## Frases de encuadre, listas para pegar

Se añaden al prompt después del bloque de estilo.

### Texto abajo (1:1, 4:5)

```
Encuadre: el sujeto ocupa los dos tercios superiores, desplazado hacia arriba.
El tercio inferior queda en negro casi puro, limpio y sin detalle, con la
incandescencia apagándose antes de llegar a él. Composición vertical 4:5.
```

### Texto a la izquierda (1.91:1, 16:9)

```
Encuadre: el sujeto ocupa el tercio derecho del cuadro. Los dos tercios
izquierdos quedan en negro casi puro, limpios y sin detalle, con un halo
apagándose desde la derecha. Composición horizontal 16:9.
```

### Story (9:16)

```
Encuadre: composición vertical 9:16. El sujeto ocupa la mitad superior,
centrado. La mitad inferior se disuelve en negro limpio. Deja libre el 15 %
superior y el 20 % inferior: ahí caen la interfaz de la aplicación y los
botones.
```

### Sin texto — la imagen se sostiene sola

```
Encuadre: el sujeto centrado, con aire alrededor. Los bordes del cuadro se
funden en negro.
```

---

## Piezas de redes con el texto ya compuesto

Cuando la pieza se maqueta con la retícula de
[`prompts/imagen/texto-en-imagen.md`](../imagen/texto-en-imagen.md), el carril
limpio no es «el tercio inferior» genérico: es el que corresponda al anclaje que
lleve esa pieza.

| Anclaje | Qué se le pide al motor |
|---|---|
| **Alto** | «La mitad superior queda en negro casi puro, limpio y sin detalle. El sujeto ocupa la mitad inferior y su incandescencia se apaga antes de subir.» |
| **Medio** | «El sujeto se abre hacia los bordes y hacia el tercio superior. La banda central del cuadro queda en negro limpio, con la luz muriendo antes de entrar en ella.» |
| **Bajo** | «El sujeto ocupa los dos tercios superiores, desplazado hacia arriba. El tercio inferior queda en negro casi puro, limpio y sin detalle.» |

### Las dos bandas reservadas van PRIMERO

En las tres, dos zonas se dejan libres siempre, porque ahí caen el símbolo y el
wordmark. **Y se piden al principio del encuadre, no al final.**

```
Encuadre: los 180 píxeles superiores y los 160 inferiores del cuadro quedan en
negro limpio, sin ninguna forma, resplandor ni reflejo — ni siquiera difuso. El
sujeto vive entre esas dos bandas y su luz se apaga antes de tocarlas.
[y aquí sigue el encuadre del anclaje que toque]
```

> **Por qué al principio, y medido.** En la primera pieza producida con este
> sistema, la banda reservada iba en la última frase del encuadre y el motor la
> ignoró: metió el sujeto incandescente justo detrás del símbolo. El 39 % de los
> píxeles de esa banda salieron por encima de 60 de luminancia, con picos de 113,
> y el símbolo naranja quedó sobre un resplandor naranja.

**El velo no lo arregla.** Se probó subir el velo en esa banda y la mejora fue de
52 a 43 de luminancia media: insuficiente, y a costa de apagar la imagen entera.
Si el fondo invade la banda reservada, **se regenera el fondo.** No se tapa.

---

## Zonas seguras

Lo que las interfaces tapan y hay que dejar libre:

- **Story / Reel:** 15 % superior (nombre de usuario) y 20 % inferior (barra de
  respuesta, botones, pie de anuncio).
- **Feed 4:5:** unos 60 px del borde inferior si el anuncio lleva botón.
- **Todo formato:** deja los bordes en negro. Con este sistema visual sale gratis
  —los negros profundos ya se comen los bordes— y perdona cualquier recorte
  automático.

---

## Cómo se pide el hueco, y cómo no

```
✗  deja espacio para el texto
✗  con área de copia
✗  negative space for headline
```

Los motores interpretan «espacio» como «zona vacía gris» y meten un degradado
plano feo.

```
✓  el tercio inferior queda en negro casi puro, limpio y sin detalle, con la
   incandescencia apagándose antes de llegar a él
```

Se describe **qué hay** en esa zona (negro limpio, la luz muriendo), no que falta
algo. Es la diferencia entre un hueco que parece intencionado y uno que parece un
error de composición.

---

## Después de generar

1. **Mira el hueco antes de maquetar.** El motor deja detalle en la zona limpia
   más o menos una vez de cada tres.
2. **Comprueba el recorte cuadrado.** Casi toda pieza vertical se va a ver
   recortada a 1:1 en algún sitio. Si el sujeto se parte, el encuadre está mal
   aunque la imagen sea buena.
3. **El texto se compone encima**, nunca en la fuente del editor por defecto.
   En web y anuncios, Archivo 600 en versalitas con tracking `-0.02em`. En
   piezas de redes manda la escala de
   [`prompts/imagen/texto-en-imagen.md`](../imagen/texto-en-imagen.md), donde el
   titular es Antonio 700.
