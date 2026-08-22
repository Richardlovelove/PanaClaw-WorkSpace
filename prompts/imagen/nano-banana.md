# Imagen · Nano Banana

Estructura para el modelo de imagen de Gemini («Nano Banana») y, en general, para
cualquier motor conversacional de imagen.

**Antes de escribir un prompt:** [`prompts/README.md`](../README.md) para la
anatomía, y los bloques de [`bloques/`](../bloques/) para el estilo, los
negativos y el encuadre.

---

## Cómo se comporta este motor

Cuatro cosas que cambian cómo se escribe el prompt:

1. **Prefiere prosa a listas de etiquetas.** Un párrafo descriptivo rinde mejor
   que `dark, orange, cinematic, 8k, masterpiece`. Nada de amontonar palabras
   sueltas ni de «8k, ultra detailed».
2. **No tiene campo de negativos separado.** Los negativos van dentro del prompt,
   en prosa. Usa la versión en prosa de [`bloques/negativos.md`](../bloques/negativos.md).
3. **Es conversacional.** Puedes corregir sobre el resultado —«más oscuro el
   tercio inferior», «quita el reflejo de la izquierda»— en vez de reescribir el
   prompt entero. Aprovéchalo: es la vía rápida para clavar el encuadre.
4. **Respeta bien los hex si se los das explícitos**, y bastante mal los nombres
   de color. Siempre `#FF5100`, nunca «naranja».

---

## Plantilla

```
[SUJETO: una frase física y concreta]

[ESCENA: dónde está, qué hace la luz, qué material es]

Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101, casi sin iluminación ambiente. La única luz nace del
propio sujeto: brasas y filamentos incandescentes en naranja #FF5100 y rojo
#FF1E1E. Materiales: obsidiana pulida, cristal negro, roca fundida, metal
oscuro con vetas encendidas. Contraste altísimo, negros profundos que se
tragan los bordes del encuadre, reflejos especulares muy contenidos.
Atmósfera de estudio, aire limpio, sin niebla lechosa. Grano fino de película.
Sin personas.

[ENCUADRE: proporción y dónde queda el negro limpio]

No incluyas: personas, oficinas, laptops ni pantallas; ningún azul, verde,
morado ni tono pastel; nada de blanco puro ni fondos claros; nada de luz
natural ni exteriores; ningún texto, letra, número, icono, logotipo ni
gráfico; nada de estética de stock corporativo.
```

Los bloques de estilo y negativos van **literales**. Solo se resuelven el sujeto,
la escena y el encuadre.

---

## Ejemplos resueltos

Tres, uno por producto, para ver cómo queda la plantilla rellenada. **No son
prompts de catálogo para reutilizar tal cual**: son la demostración de la forma.

### Velocidad · Sitios web · feed 4:5

```
Un proyectil de obsidiana pulida atravesando el cuadro a velocidad extrema,
dejando estelas de luz que se estiran detrás de él.

La superficie del proyectil refleja las propias estelas. El aire alrededor está
completamente oscuro; solo se ve lo que la estela ilumina a su paso. La forma
es aerodinámica y sin marcas, como una gota de piedra negra.

Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101, casi sin iluminación ambiente. La única luz nace del
propio sujeto: brasas y filamentos incandescentes en naranja #FF5100 y rojo
#FF1E1E. Materiales: obsidiana pulida, cristal negro, roca fundida, metal
oscuro con vetas encendidas. Contraste altísimo, negros profundos que se
tragan los bordes del encuadre, reflejos especulares muy contenidos.
Atmósfera de estudio, aire limpio, sin niebla lechosa. Grano fino de película.
Sin personas.

Encuadre: el sujeto ocupa los dos tercios superiores, desplazado hacia arriba
y entrando por la derecha. El tercio inferior queda en negro casi puro, limpio
y sin detalle, con la incandescencia apagándose antes de llegar a él.
Composición vertical 4:5.

No incluyas: personas, oficinas, laptops ni pantallas; ningún azul, verde,
morado ni tono pastel; nada de blanco puro ni fondos claros; nada de luz
natural ni exteriores; ningún texto, letra, número, icono, logotipo ni
gráfico; nada de estética de stock corporativo.
```

### Seguridad · story 9:16 · variante fría

```
Tres monolitos de piedra negra alzados sobre una llanura fracturada. Por las
grietas de cada monolito corren circuitos rojos que se están apagando.

La llanura se pierde en la oscuridad a pocos metros. Las fisuras del suelo
también brillan, más tenues, como si la energía se estuviera drenando hacia
abajo. Nada se mueve.

Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101, casi sin iluminación ambiente. La única luz nace del
propio sujeto: brasas y filamentos incandescentes en naranja #FF5100 y rojo
#FF1E1E. Materiales: obsidiana pulida, cristal negro fracturado, metal oscuro
con circuitos rojos apagándose. La incandescencia es más escasa y más
distante. Contraste altísimo, negros profundos que se tragan los bordes del
encuadre, reflejos especulares muy contenidos. Atmósfera de estudio, aire
limpio, sin niebla lechosa. Grano fino de película. Sin personas.

Encuadre: composición vertical 9:16. Los monolitos ocupan la mitad superior,
centrados. La mitad inferior se disuelve en negro limpio. Deja libre el 15 %
superior y el 20 % inferior.

No incluyas: personas, oficinas, laptops ni pantallas; ningún azul, verde,
morado ni tono pastel; nada de blanco puro ni fondos claros; nada de luz
natural ni exteriores; ningún texto, letra, número, icono, logotipo ni
gráfico; nada de estética de stock corporativo; nada de candados, escudos ni
iconos de seguridad.
```

> Fíjate en la última línea: cuando el tema es seguridad, **hay que añadir
> candados y escudos a los negativos**. Es el cliché al que se va el motor sin
> falta.

### eBot · OpenGraph 1.91:1 · variante íntima

```
Una mano tallada en cristal negro —claramente no humana, facetada como una
gema— extendida hacia una esfera de datos incandescente que flota a unos
centímetros de sus dedos.

La esfera está hecha de filamentos de luz entrelazados que giran despacio. Su
resplandor se refracta dentro del cristal de la mano y la enciende por dentro.
El punto de contacto todavía no ocurre.

Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101, casi sin iluminación ambiente. La única luz nace del
propio sujeto: brasas y filamentos incandescentes en naranja #FF5100 y rojo
#FF1E1E. Materiales: obsidiana pulida, cristal negro, roca fundida, metal
oscuro con vetas encendidas. Contraste altísimo, negros profundos que se
tragan los bordes del encuadre, reflejos especulares muy contenidos. Plano
cercano, profundidad de campo corta, el fondo se disuelve en negro a pocos
centímetros del sujeto. Grano fino de película. Sin personas.

Encuadre: el sujeto ocupa el tercio derecho del cuadro. Los dos tercios
izquierdos quedan en negro casi puro, limpios y sin detalle, con un halo
apagándose desde la derecha. Composición horizontal 1.91:1.

No incluyas: personas, rostros, oficinas, laptops ni pantallas; ningún azul,
verde, morado ni tono pastel; nada de blanco puro ni fondos claros; nada de
luz natural ni exteriores; ningún texto, letra, número, icono, logotipo ni
gráfico; nada de estética de stock corporativo; nada de robots ni androides.
```

> Aquí `manos humanas` sale de los negativos porque el sujeto **es** una mano —
> y se compensa describiéndola como no humana dos veces, en el sujeto y en los
> negativos (`nada de robots ni androides`).

---

## El carrusel es un solo fondo, cortado

> **No se genera un fondo por diapositiva.** Se genera uno y se parte.

Es la diferencia entre un carrusel que al deslizar sigue siendo el mismo objeto y
tres imágenes que comparten paleta. Y no se arregla describiendo la misma escena
tres veces: este motor devuelve tres imágenes **parecidas y distintas**, con la
luz en otro sitio y el material con otro brillo. La costura canta.

Dos maneras, y las decide el número de diapositivas:

| Diapositivas | Cómo | Por qué |
|---|---|---|
| **2 o 3** | **Panorámica cortada** | Cabe en una proporción que el motor entrega |
| **4 o más** | **Cadena de relevo** | Ya no cabe: haría falta 3.2:1 o más |

---

### Panorámica cortada · 2 o 3 diapositivas

Se pide **una sola imagen ancha** y se corta en trozos de 1080.

| Diapositivas | Lienzo final | Se pide | Sobra |
|---|---|---|---|
| 3 | 3240 × 1350 | **21:9** | 38 px de alto, 19 arriba y 19 abajo |
| 2 | 2160 × 1350 | **3:2** | 90 px de alto |

**Para dos no sirve 21:9:** escalada a 2160 de ancho se queda en 925 de alto y no
cubre los 1350. Hay que pedirla menos apaisada.

Tres cosas cambian respecto de un encuadre normal, y las tres van dentro del
prompt:

1. **Las bandas reservadas cruzan la panorámica entera.** El símbolo y el
   wordmark van en todas las diapositivas, así que las dos franjas se piden de
   lado a lado, no por trozo.
2. **El carril del texto es una franja horizontal continua.** El anclaje no
   salta entre diapositivas, así que el hueco limpio tampoco: es una banda que
   recorre toda la panorámica a la misma altura.
3. **El punto focal de cada trozo cae en su centro, no en sus bordes.** Por los
   cortes pasa materia continua —una estela, el cuerpo del sujeto, la caída de
   la luz—, nunca el detalle que hay que mirar. Al deslizar, la aplicación mete
   un hueco entre diapositivas: lo que esté partido justo ahí se lee roto.

Y el recorrido: **el sujeto avanza de izquierda a derecha** —el sentido en que se
desliza— y **la luz va en un solo sentido**: o crece o se apaga a lo largo del
cuadro. Nunca sube, baja y vuelve a subir.

#### Ejemplo resuelto · carrusel de 3, velocidad, anclaje bajo

```
Un proyectil de obsidiana pulida cruzando el cuadro de izquierda a derecha,
dejando estelas de luz que se estiran detrás de él a lo largo de todo el
encuadre.

En el tercio izquierdo el proyectil apenas está entrando y las estelas son
cortas y tenues. En el tercio central lo cruza entero, con las estelas ya
largas y brillantes. En el tercio derecho el proyectil se detiene y las
estelas lo alcanzan y se apagan contra él. La superficie del proyectil
refleja sus propias estelas. La forma es aerodinámica y sin marcas, como una
gota de piedra negra.

Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101, casi sin iluminación ambiente. La única luz nace del
propio sujeto: brasas y filamentos incandescentes en naranja #FF5100 y rojo
#FF1E1E. Materiales: obsidiana pulida, cristal negro, roca fundida, metal
oscuro con vetas encendidas. Contraste altísimo, negros profundos que se
tragan los bordes del encuadre, reflejos especulares muy contenidos.
Atmósfera de estudio, aire limpio, sin niebla lechosa. Grano fino de
película. Sin personas.

Encuadre: composición horizontal 21:9, muy apaisada, pensada para leerse
como una sola escena continua de izquierda a derecha. La franja superior y
la franja inferior del cuadro quedan en negro limpio de lado a lado, sin
ninguna forma, resplandor ni reflejo, ni siquiera difuso. El tercio inferior
del cuadro entero queda en negro casi puro, limpio y sin detalle, de un
extremo al otro y a la misma altura en todo el ancho, con la incandescencia
apagándose antes de bajar hasta él. El sujeto vive en la mitad superior.
Reparte el interés en tres momentos: uno centrado en el tercio izquierdo,
uno en el centro y uno en el tercio derecho. Justo en el primer tercio y en
los dos tercios del ancho no debe haber ningún detalle que llame la
atención: por ahí solo pasan las estelas.

No incluyas: personas, oficinas, laptops ni pantallas; ningún azul, verde,
morado ni tono pastel; nada de blanco puro ni fondos claros; nada de luz
natural ni exteriores; ningún texto, letra, número, icono, logotipo ni
gráfico; nada de estética de stock corporativo.
```

> **Fíjate en «justo en el primer tercio y en los dos tercios del ancho».** Eso
> son los dos cortes. Nombrarlos como fracciones del ancho es la única forma que
> tiene el motor de entenderlos: no sabe qué es una diapositiva.

---

### Cadena de relevo · 4 diapositivas o más

Por encima de tres, la panorámica pediría 3.2:1 o más y ningún motor la entrega.
Escalar una 21:9 hasta ahí obliga a tirar más de un tercio del alto, y con él el
encuadre con el que se compuso.

Así que se encadena, **aprovechando que este motor es conversacional**: se genera
la primera y cada siguiente se pide **con la anterior delante**, en el mismo hilo.

```
Turno 1   El prompt completo de la primera diapositiva, 4:5.

Turno 2   Con la imagen anterior delante:
          «Misma escena, misma cámara, misma luz y mismo material. La cámara
          ha seguido avanzando hacia la derecha: el borde izquierdo de la
          imagen nueva continúa el borde derecho de esta. El sujeto ha
          avanzado y ahora ocupa el centro. Mantén el tercio inferior en
          negro limpio a la misma altura. Composición vertical 4:5.»

Turno 3…  Igual, siempre con la ANTERIOR delante — no con la primera.
```

**Siempre con la anterior, nunca con la primera.** Encadenando contra la primera,
la tercera y la cuarta se van pareciendo cada vez menos a su vecina, que es
justo la unión que se ve al deslizar.

**La cadena no da continuidad de píxel, y no pasa nada.** Lo que tiene que
sobrevivir es el material, la temperatura de la luz y la dirección del
movimiento. Si eso se mantiene, el carrusel se lee como uno.

---

### Antes de dar el fondo de un carrusel por bueno

- [ ] ¿Es **una** imagen cortada, o son N imágenes?
- [ ] Ponlas en tira, pegadas por el borde. ¿Se ve alguna costura?
- [ ] ¿Hay un escalón de brillo en algún corte?
- [ ] ¿Hay un punto focal partido justo por un corte?
- [ ] ¿El carril limpio está a la misma altura en las N?
- [ ] ¿El sujeto avanza hacia la derecha y se detiene en la última?
- [ ] ¿La luz va en un solo sentido, sin subir y volver a bajar?

---

## Qué sale mal, y cómo se corrige

Los cinco fallos que se repiten. La columna derecha es lo que se le dice al
motor en el turno siguiente, sin reescribir el prompt.

| Sale | Se dice |
|---|---|
| El tercio limpio tiene detalle o degradado | «El tercio inferior tiene que ser negro plano, sin ninguna forma ni degradado visible.» |
| El naranja se fue a amarillo o a rojo puro | «El acento es exactamente #FF5100. Corrige la temperatura de la luz a ese valor.» |
| Metió iluminación ambiente | «Quita toda luz externa. Lo único que ilumina la escena es la incandescencia del propio sujeto.» |
| Aparecen personas o siluetas | «Elimina cualquier figura humana o silueta que parezca una persona.» |
| Aparece texto inventado en la imagen | «Elimina todo texto, letra y número de la imagen.» |
| En la panorámica, el carril limpio sube y baja | «El tercio inferior tiene que quedar en negro limpio a la MISMA altura de un extremo al otro del cuadro.» |
| El punto focal cayó justo en un corte | «Desplaza el sujeto hacia el centro de su tercio. Justo en el primer tercio y en los dos tercios del ancho solo pueden pasar estelas.» |

**Los tres primeros son los habituales.** Si el motor falla el hex dos veces
seguidas, pásale el prompt en inglés
([`bloques/estilo-visual.md`](../bloques/estilo-visual.md) trae la traducción
oficial).

---

## El texto se compone encima, nunca se genera

**No le pidas a este motor que escriba el titular.** Escribe mal en español
—come tildes y convierte la eñe— y no reproduce la tipografía de la marca. En
un mes de contenido normal, más de la mitad de los titulares llevan tilde, eñe o
signo de apertura: no es un riesgo ocasional, es la mayoría de las piezas.

Lo que sí hace bien es dejar el hueco. Después, según dónde vaya la pieza:

- **Web, anuncios, correo:** Archivo 600, versalitas, tracking `-0.02em`,
  `#FFF7F7`. Antetítulo Archivo 400, 14 px, tracking `0.16em`, `#FF5100`.
  Bajada Archivo 300, `#BABABA`.
- **Redes sociales:** manda la escala completa de
  [`prompts/imagen/texto-en-imagen.md`](texto-en-imagen.md), donde el titular es
  Antonio 700 y hay una retícula en píxeles.

---

## Antes de dar la imagen por buena

- [ ] ¿El fondo es negro cálido y no negro puro ni gris?
- [ ] ¿El acento es `#FF5100` y no amarillo ni rojo?
- [ ] ¿Hay algún azul, verde o blanco puro colado?
- [ ] ¿El hueco del texto está realmente limpio?
- [ ] ¿Se sostiene si alguien la recorta a 1:1?
- [ ] ¿Hay alguna persona, silueta, logo o texto inventado?
