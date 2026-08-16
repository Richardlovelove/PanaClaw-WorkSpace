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

### Botón de descarga

Cada pieza lleva su botón que la baja en PNG a tamaño real, dibujando la imagen
y el texto sobre un `<canvas>` de 1080×1350. Sin librerías externas: el lienzo
del navegador dibuja texto con tildes sin ningún problema, y las fuentes ya
están cargadas.

Y un botón que las descargue todas de una.

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

**Cuenta los hashtags de cada pieza.** Es lo que más se le va: le das seis y
devuelve nueve.

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
