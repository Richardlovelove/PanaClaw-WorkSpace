# Plataforma · Meta AI

Meta AI se usa para **dos cosas y ninguna más**: generar los fondos y montar el
documento HTML donde se ven las piezas ya compuestas y se descargan.

**No escribe una sola palabra de la marca.** Ese es el contrato entero de este
archivo, y hay una razón medida detrás.

---

## Lo que hace bien

1. **Genera el mundo visual.** La estética de materia oscura incandescente le
   sale a la primera y bastante consistente entre piezas.
2. **Devuelve un documento HTML completo**, con las imágenes dentro del propio
   archivo. Es lo que lo separa de un generador suelto: entrega el lote entero
   en un archivo que se abre en el navegador y no depende de nada externo.
3. **Sostiene la retícula si se la das en píxeles.** Si le das «x=72, y=248,
   132 px, interlínea 0.88» la respeta. Si le dices «bien maquetado», improvisa.
   Lo mismo con la holgura de las tildes: la aplica si se la das como cuenta, y
   la ignora si se la pides como criterio.

## Lo que hace mal, con la prueba delante

**Inventa datos con total fluidez y formato perfecto.** No es una sospecha: es lo
que devolvió la última vez que se le pasó un plan de contenido para que lo
maquetara, en la misma entrega que por lo demás estaba bien.

| Lo que escribió | Lo que es cierto |
|---|---|
| «$295 incluye dominio + alojamiento + código fuente primer año» | El dominio se renueva aparte, unos $15 al año |
| «entrega en 7 a 10 días» | Start entrega en 72 h |
| «cada segundo de carga = 7% menos conversión» | Nadie midió eso |
| «tu sitio tarda 4 segundos, pierdes 28% de ventas» | Nadie midió eso |
| «no usamos 47 complementos» | Cifra inventada |
| «nuestro proceso tiene 6 puertas» | Ese proceso no existe en el catálogo |
| «accesos: cpanel, ftp, base de datos» | No es lo que se entrega |
| Ocho hashtags por publicación | El tope son seis |

Ocho invenciones en doce publicaciones. Todas verosímiles, todas con la cifra
bien puesta, ninguna cierta. **Un modelo que inventa el 60 % de las piezas no
puede escribir el copy de una marca cuyo argumento es que no hay letra chica.**

De ahí sale la única regla dura de este archivo.

---

## El reparto del trabajo

```
CLAUDE          escribe el 100 % del texto, verificado contra datos/precios.json
  ↓             titulares, descripciones, hashtags, cortes de línea, qué va naranja
META AI         genera los fondos y monta el HTML
  ↓             copia el texto LITERAL. No lo redacta, no lo mejora, no lo acorta
HUMANO          descarga los PNG y publica
```

**Meta recibe el texto ya escrito y su trabajo es pegarlo, no producirlo.** La
instrucción que lo cierra va literal en el prompt maestro:

```
No escribas, no redactes, no completes, no acortes, no traduzcas y no
"mejores" ningún texto. Todo el texto de este documento ya está escrito más
abajo. Cópialo carácter por carácter, con sus tildes, sus eñes y sus puntos
finales. Si algo te parece incompleto, déjalo como está: está así a propósito.
No añadas ninguna cifra, porcentaje, estadística, plazo, testimonio ni
beneficio que no esté escrito literalmente en este documento.
```

Esa frase es lo primero que se comprueba al revisar lo que devuelva.

---

## El contrato del HTML

Lo que el documento tiene que traer. Va en el prompt maestro tal cual.

### Fuentes

```
Carga Antonio y Archivo desde Google Fonts:
https://fonts.googleapis.com/css2?family=Antonio:wght@700&family=Archivo:wght@300;400;500;700&display=swap
```

Sin esas dos, todo lo demás da igual: el navegador cae a una fuente del sistema
y la pieza deja de ser de la marca.

### Cada pieza, compuesta y a medida real

Cada diapositiva se dibuja a **1080×1350 exactos** —no «aproximadamente
vertical»— con la imagen de fondo a sangre, el velo encima y el texto compuesto
según [`prompts/imagen/texto-en-imagen.md`](../imagen/texto-en-imagen.md). En
pantalla se puede ver reducida con `transform: scale()`, pero el lienzo que se
exporta mide 1080×1350.

### El titular se compone línea a línea, con su holgura

**Cada línea del titular es su propio elemento.** Los cortes ya vienen decididos
en el texto de la pieza; el navegador no parte ninguna línea.

Y **el avance entre dos líneas no es un número fijo**: es una cuenta que depende
de lo que lleve cada una. La razón, medida en píxeles, está en
[`prompts/imagen/texto-en-imagen.md`](../imagen/texto-en-imagen.md). Esto es lo
que va literal en el prompt maestro:

```
Cada línea del titular es su propio bloque. La interlínea base es la de su
tamaño (0.88 en XL y L, 0.90 en M) y NO se aplica igual a todas las líneas:

  avance(n → n+1) = base
                  + 0.27  si la línea n+1 lleva Á, É, Í, Ó o Ú
                  + 0.20  si la línea n+1 lleva Ñ o Ü
                  + 0.17  si la línea n   lleva Q, ¿, ¡ o coma

Las tres se suman cuando coinciden. En HTML esa holgura es un margen
superior en «em» sobre la línea que la necesita, con la interlínea base
puesta en el bloque. En el lienzo de exportación es ese mismo valor sumado
al avance vertical de esa línea.

Antonio no rebaja los acentos en versalitas: la tilde de una Á sube 0.27 em
por encima de la letra. Sin esa holgura la tilde cae DENTRO de las letras de
la línea de arriba — 27 píxeles a tamaño 112 — y la pieza sale con las
líneas comidas. No subas la interlínea de todas las líneas para arreglarlo:
afloja el bloque entero y deja de ser el titular de esta marca.

El bloque de texto no lleva recorte de ningún tipo. Con interlínea por
debajo de 1, la tinta de la primera línea sale por encima de su caja de
línea, y cualquier recorte le rasura la tilde.
```

### Botón de descarga

Cada pieza lleva su botón que la baja en PNG a tamaño real, dibujando la imagen
y el texto sobre un `<canvas>` de 1080×1350. Sin librerías externas: el lienzo
del navegador dibuja texto con tildes sin ningún problema, y las fuentes ya
están cargadas.

Y un botón que las descargue todas de una.

### Las siete trampas del exportador

**Aquí es donde falla, y falla en silencio: la vista previa se ve perfecta y el
PNG sale roto.** Estas siete van literales en el prompt maestro, porque no son
gustos — son fallos observados en un documento que por lo demás estaba bien.

```
1. ctx.letterSpacing NO se reinicia al cambiar ctx.font. Si lo usas para el
   tracking del wordmark, ponlo a '0px' inmediatamente después de dibujarlo.
   Si no, el tracking se filtra a la cifra, al antetítulo y al titular, y el
   titular se sale del lienzo.

2. Fija ctx.textBaseline='top' antes de dibujar y usa la misma Y que el
   maquetado. Con el valor por defecto ('alphabetic') el texto del PNG cae
   más abajo que en la vista previa.

3. Mide el alto real del bloque de texto con getBoundingClientRect() del
   elemento ya maquetado. No lo estimes multiplicando líneas por interlínea:
   el anclaje al centro óptico se descuadra respecto a lo que se ve.

4. El símbolo EMPIEZA en y=96, no está centrado en y=96. Su caja va de 96 a
   168, y mide 88 de ancho por 72 de alto. No es cuadrado.

5. Un botón que lanza una descarga por pieza, todas seguidas, lo bloquea el
   navegador a la tercera. O agrupas en un ZIP de verdad, o el botón se llama
   "descargar una por una" y avisa de que hay que permitirlo.

6. El avance vertical entre líneas del titular NO es líneas × interlínea.
   Lleva la holgura de las tildes sumada línea a línea. Acumula el avance
   real; si lo calculas multiplicando, el PNG sale con las líneas comidas
   aunque la vista previa esté bien, o al revés.

7. En un carrusel, el fondo de cada diapositiva es un TROZO de una sola
   imagen. Se dibuja la panorámica entera desplazada −1080·k, no una imagen
   por diapositiva. Si recortas y reescalas cada trozo por separado, los
   redondeos dejan una línea de costura de uno o dos píxeles en cada corte.
```

**Y una comprobación que el humano hace, no el modelo:** descarga una pieza y
ponla al lado de su vista previa. Si no son idénticas, el exportador está mal y
lo están todas las del lote.

### Un carrusel se monta como una tira

Un carrusel **no son N piezas seguidas en el documento**: es una pieza larga
cortada. El documento tiene que dejar ver las dos cosas — la tira entera para
juzgar la continuidad, y cada diapositiva suelta para descargarla.

Va literal en el prompt maestro:

```
Un carrusel se muestra DOS veces en el documento:

1. Primero la tira: las N diapositivas en fila, pegadas por el borde, sin
   ninguna separación, margen ni borde entre ellas, reducidas para que
   quepan a lo ancho. Es la única vista donde se ven las costuras.

2. Debajo, cada diapositiva por separado, a su tamaño de vista previa y con
   su botón de descarga.

El fondo del carrusel es UNA sola imagen panorámica que cubre 1080×N de
ancho por 1350 de alto. La diapositiva k NO lleva su propia imagen: lleva la
panorámica entera desplazada −1080·k. En la vista previa eso es una imagen
de fondo con background-position; en el lienzo de exportación es la misma
imagen dibujada con ese mismo desplazamiento.

El velo es vertical y con exactamente los mismos valores en las N
diapositivas. El brillo de la imagen es exactamente el mismo número en las
N. Si cambia entre diapositivas, aparece un escalón en cada costura.

El antetítulo, el anclaje del bloque de texto y el tamaño del titular no
cambian entre diapositivas del mismo carrusel salvo que el texto de cada una
lo diga.

El numerador va ENCENDIDO en carrusel: esquina superior derecha, x=1008,
formato 01/05, color #BABABA.
```

**Por qué la tira va primero.** Una diapositiva suelta puede estar perfecta y
romper el carrusel: un escalón de brillo o un punto focal partido por la mitad
solo se ven con las N pegadas. Si el documento no las enseña juntas, ese fallo
llega a la publicación.

### El resto del documento

Debajo de cada pieza, en texto seleccionable para copiar y pegar:

- La **descripción** de la publicación, tal cual
- Los **hashtags**, tal cual
- El **prompt del fondo**, por si hay que regenerar esa imagen

### La interfaz del documento

Fondo `#100101`, texto `#FFF7F7`, acento `#FF5100`. Es una herramienta interna,
pero se ve todo el mes: si el documento es feo, las piezas parecen feas.

---

## Cómo se le pide

El prompt maestro lo arma
[`skills/contenido-instagram/SKILL.md`](../../skills/contenido-instagram/SKILL.md).
El orden importa y es este:

```
1. QUÉ ERES Y QUÉ NO HACES      el reparto del trabajo, la prohibición de escribir
2. EL SISTEMA VISUAL            hex, tipografías, retícula, escala, velo
3. EL CONTRATO DEL HTML         fuentes, medidas, descarga
4. EL BLOQUE DE ESTILO          literal, de bloques/estilo-visual.md
5. LOS NEGATIVOS                literal, de bloques/negativos.md
6. LAS PIEZAS                   una por una, con su texto ya escrito y su fondo
7. LA VERIFICACIÓN              lo que tiene que comprobar antes de devolver
```

**La prohibición de escribir va la primera y se repite en la séptima.** Una sola
vez, al principio de un prompt largo, se le olvida a la mitad.

---

## Qué revisar cuando devuelva el documento

Los cinco fallos, por frecuencia:

| Fallo | Cómo se ve | Qué se le dice |
|---|---|---|
| **Reescribió un texto** | Una descripción que suena parecida pero no igual | «El texto de la pieza N no coincide con el que te di. Cópialo literal.» |
| **Añadió una cifra** | Un porcentaje o una estadística que no le diste | «Quita el dato de la pieza N. No estaba en lo que te pasé.» |
| **Se comió una tilde** | «CODIGO TUYO» | «Faltan tildes en la pieza N. El texto correcto es: …» |
| **Metió texto en la imagen** | Letras dentro del fondo generado | «El fondo de la pieza N tiene letras. Regenéralo sin ningún texto.» |
| **El lienzo no mide 1080×1350** | El PNG descargado sale de otro tamaño | «El lienzo de exportación tiene que ser exactamente 1080×1350.» |
| **Aplicó la interlínea igual a todas las líneas** | Una tilde o una eñe metida dentro de las letras de la línea de encima | «Falta la holgura del titular de la pieza N. La línea que lleva la tilde avanza 0.27 más; la que lleva eñe, 0.20; y la que va debajo de una Q o un signo de apertura, 0.17 más.» |
| **Subió la interlínea de todas** | El bloque del titular se ve suelto y ya no compacto | «La interlínea base sigue siendo 0.88. La holgura va solo en las líneas que la necesitan.» |
| **Generó un fondo por diapositiva** | Al poner el carrusel en tira, cada corte es una imagen distinta | «El fondo del carrusel es una sola panorámica cortada. Usa la misma imagen desplazada −1080·k en cada diapositiva.» |
| **Cambió el brillo entre diapositivas** | Un escalón de luz en la costura | «El brillo de la imagen es el mismo número en las N diapositivas.» |

**Cuenta los hashtags de cada pieza.** Es lo que más se le va: le das seis y
devuelve nueve.

**Y mira los carruseles en tira antes que sueltos.** Las costuras no se ven de
ninguna otra manera.

---

## Lo que no se le pide nunca

- Que escriba, sugiera o mejore copy
- Que proponga publicaciones que no estén en el plan
- Que ajuste un precio «para que se lea mejor»
- Que resuma la lista de lo que NO incluye
- Que traduzca al inglés
- Que añada emojis a un titular o dentro de una imagen

Nada de lo que devuelva se publica sin pasar por
[`orquestador/protocolo-entrega.md`](../../orquestador/protocolo-entrega.md).
