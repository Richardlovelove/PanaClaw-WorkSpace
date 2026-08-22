# Bloque · Negativos

Lo que no puede aparecer. Se pega en todo prompt de imagen y de video, en la
forma que entienda el motor.

**No es una lista de gustos.** Cada entrada tapa un fallo concreto que los
generadores cometen por defecto cuando les pides «una imagen para una agencia
web».

---

## Versión para motores con campo de negativos separado

Pégalo tal cual en el campo `negative prompt`:

```
personas, gente, rostros, manos humanas, equipos de trabajo, oficinas,
escritorios, laptops, monitores con interfaces, teclados, sillas de oficina,
azul, cian, turquesa, verde, morado, amarillo, rosa, tonos pastel, blanco puro,
fondos claros, fondos blancos, degradados multicolor, arcoíris, luz natural,
luz de ventana, luz diurna, cielo, exteriores, plantas, madera clara,
minimalismo escandinavo, ilustración plana, vector, 3D de dibujos animados,
iconos, logotipos, marcas de agua, texto, letras, números, tipografía,
gráficos, tablas, flechas, infografías, collage, marco, borde, viñeta blanca,
stock corporativo, apretón de manos, gráfico de barras subiendo, bombilla,
engranajes, nube con rayo, código en pantalla, terminal, matriz de números
verdes
```

## Versión en inglés

```
people, humans, faces, human hands, teams, offices, desks, laptops, monitors
with UI, keyboards, office chairs, blue, cyan, teal, green, purple, yellow,
pink, pastel colors, pure white, bright backgrounds, white backgrounds,
multicolor gradients, rainbow, natural light, window light, daylight, sky,
outdoors, plants, light wood, scandinavian minimalism, flat illustration,
vector art, cartoon 3D, icons, logos, watermarks, text, letters, numbers,
typography, charts, tables, arrows, infographics, collage, frame, border,
white vignette, corporate stock, handshake, rising bar chart, lightbulb, gears,
cloud with lightning bolt, code on screen, terminal, green digital rain
```

## Versión en prosa

Para motores que no tienen campo de negativos (Nano Banana entre ellos). Va al
final del prompt, como una frase más:

```
No incluyas: personas, oficinas, laptops ni pantallas; ningún azul, verde,
morado ni tono pastel; nada de blanco puro ni fondos claros; nada de luz
natural ni exteriores; ningún texto, letra, número, icono, logotipo ni gráfico;
nada de estética de stock corporativo.
```

---

## Los cinco grupos, y por qué

### 1 · Personas y oficina

`personas · rostros · manos humanas · equipos · oficinas · escritorios ·
laptops · monitores · teclados`

No hay gente en el sistema visual de PanaClaw. Es la instrucción que más se
ignora, así que va **duplicada**: en el bloque de estilo (`Sin personas`) y aquí.

*Única excepción tolerada:* una **mano de cristal oscuro**, que ya existe en el
sitio y no lee como humana. Si la pides, dilo explícitamente en el sujeto:
«una mano tallada en cristal negro, claramente no humana».

### 2 · Color fuera de paleta

`azul · cian · verde · morado · amarillo · rosa · pastel · blanco puro ·
degradados multicolor`

El azul es el primero de la lista a propósito: es el color por defecto de todo lo
que un generador asocia con «tecnología», y es exactamente la categoría contra la
que se posiciona la marca.

### 3 · Luz equivocada

`luz natural · luz de ventana · luz diurna · cielo · exteriores · fondos claros`

En PanaClaw **la luz nace del sujeto**. Una escena iluminada desde fuera deja de
ser de la marca aunque acierte los colores.

### 4 · Texto y elementos gráficos

`texto · letras · números · tipografía · iconos · logotipos · gráficos · flechas ·
infografías · marcas de agua`

El texto se compone encima, nunca se genera. Los motores escriben mal en español
—tildes, eñes— y no reproducen la tipografía de la marca. Quién lo compone y con
qué medidas está en
[`prompts/imagen/texto-en-imagen.md`](../imagen/texto-en-imagen.md).

**Si la pieza sí lleva texto generado**, quita solo `texto`, `letras` y
`tipografía` de la lista. Deja los iconos, los logos y las infografías fuera.

**`logotipos` incluye el de PanaClaw, y no tiene excepción.** El motor no dibuja
el símbolo de la marca ni siquiera cuando la pieza lo lleva: el logo se compone
encima, con el trazado exacto de
[`bloques/logo.md`](logo.md). Un logo generado sale parecido —tres trazos, un
color aproximado— y parecido es otra marca. Es la regla 6 de
[`orquestador/reglas.md`](../../orquestador/reglas.md).

### 5 · Clichés de agencia

`stock corporativo · apretón de manos · gráfico de barras subiendo · bombilla ·
engranajes · nube con rayo · código en pantalla · matriz de números verdes`

Los siete lugares comunes a los que se va cualquier generador cuando le hablas de
una empresa de tecnología. Ninguno pertenece a esta marca.

---

## Qué se quita según el caso

| Caso | Quita de la lista |
|---|---|
| La pieza lleva texto generado | `texto`, `letras`, `números`, `tipografía` |
| Pides la mano de cristal | `manos humanas` (y descríbela como no humana) |
| Es una captura de producto real | `monitores con interfaces` |

Todo lo demás se queda siempre.
