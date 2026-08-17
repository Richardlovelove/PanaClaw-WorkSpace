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
