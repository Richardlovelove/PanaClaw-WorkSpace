# Protocolo de entrega

Lo que hace un agente entre «ya tengo el trabajo hecho» y «aquí lo tienes». Son
pocos minutos y evitan el tipo de fallo que solo se detecta cuando ya está
publicado.

---

## Antes de generar: los tres datos que faltan casi siempre

No empieces a producir sin esto. Preguntarlo cuesta un mensaje; adivinarlo cuesta
rehacer el entregable entero.

1. **Formato y medida exactos.** No «para Instagram» — Instagram tiene feed
   cuadrado, feed vertical 4:5, story 9:16 y reel 9:16, y no se recortan entre sí
   sin perder el titular.
2. **Producto y precio concretos.** «Anuncia los servicios» no es cotizable: hay
   seis productos con seis precios y seis públicos distintos.
3. **La única acción que quieres provocar.** Una pieza con dos llamadas a la
   acción no tiene dos, tiene cero.

Si el humano ya te dio los tres, no preguntes nada más y produce.

---

## Verificación obligatoria

Ocho comprobaciones. Se hacen **mirando el archivo**, no de memoria — la memoria
es exactamente donde se cuelan los precios viejos y donde se redibuja el logo.

### 1. Cifras

Cada importe que aparezca en el entregable existe en
[`datos/precios.json`](../datos/precios.json), con ese formato y ese rango.

- ¿Hay algún importe de pago único sumado a uno mensual? → sepáralos.
- ¿Hay algún rango citado por su mínimo a secas? → o el rango entero, o «desde».
- ¿Hay alguna cifra que salió de tu cabeza? → fuera.

### 2. Color y tipografía

Cada hex se copió de [`datos/marca.json`](../datos/marca.json).

- ¿`#FF1E1E` aparece en algún texto? → prohibido, es color de fondo.
- ¿Aparece azul, verde, morado o `#FFFFFF` puro? → fuera.
- ¿La tipografía es la que toca? Archivo en web, anuncios, correo y propuestas.
  En piezas de redes, Antonio 700 en titular y cifra y Archivo en el resto.
  **Ninguna otra familia, en ningún caso** — el verificador la caza.
### 3. El logo

Regla 6 de [`reglas.md`](reglas.md). Se comprueba en dos sitios: en el
entregable, y en el prompt que lo produjo.

**En la pieza:**

- ¿El símbolo son **seis figuras rellenas** —dos corchetes, un punto romboidal y
  tres zarpazos—, y no unos trazos parecidos? Amplía al 400 % y cuéntalas.
- ¿Los huecos de los corchetes se ven abiertos? Si es una mancha sólida, falta
  `fill-rule="evenodd"`.
- ¿Es `#FF5100` plano, con `fill` y sin ningún `stroke`?
- ¿Conserva su proporción 100 × 81.56, escalado con el mismo número en los dos
  ejes?
- ¿Lleva el wordmark su punto naranja?

**En el prompt, si el entregable es un prompt:**

- ¿Está el trazado **entero, dentro**, copiado de
  [`prompts/bloques/logo.md`](../prompts/bloques/logo.md)?
- ¿Aparece en las **dos** formas que hagan falta —el `<svg>` de la vista previa y
  el `Path2D` del lienzo que exporta?
- ¿Queda alguna frase que describa el logo en palabras o que lo mande a buscar a
  un archivo de este repositorio? → es un hueco con medidas, y se rellena solo.

### 4. Jerga

Búsqueda literal en el entregable: `Jamstack`, `CDN`, `LCP`, `SSG`, `headless`,
`stack`, `deploy`, `framework`, `Lighthouse`, `pipeline`, `onboarding`.

Cero resultados o se reescribe.

### 5. Personalidad

Tres preguntas de [`adn/05-personalidad.md`](../adn/05-personalidad.md):

- ¿Sobra el 30 %? → bórralo.
- ¿Se dice el límite **antes** de que lo pregunten? → si no, falta.
- ¿Hay ruego, urgencia, justificación del precio, o una autoridad afirmada en
  vez de demostrada? → fuera.

Y la búsqueda literal del léxico de esta capa: `premium`, `exclusivo`,
`boutique`, `VIP`, `élite`, `alta gama`, `líder`, `referente`, `los mejores`.

### 6. Promesas

- ¿Se promete posicionamiento en Google? → prohibido.
- ¿Se promete un plazo sin decir desde cuándo cuenta? → el reloj empieza cuando
  el cliente entrega material y el 50 %. Dilo en la pieza.
- ¿Hay un dato, cifra o testimonio que no puedas señalar en este repositorio? →
  fuera.

### 7. Claridad y oficio

Dos preguntas, y las dos se contestan mirando la pieza, no recordándola:

- **La prueba del rótulo.** Tapa la marca y la cifra. ¿Un dueño de negocio sabe
  qué se vende? Si hay que deducirlo, es una adivinanza →
  [`adn/06-claridad.md`](../adn/06-claridad.md) §9.
- **La prueba del descarte.** ¿El gancho funcionaría igual para otra agencia de
  Panamá? Entonces es un rótulo → [`adn/07-redaccion.md`](../adn/07-redaccion.md) §4.

Y el recorte: **¿se hizo el paso 5 del método de `07-redaccion.md` §7?** Si sí,
no se recorta otra vez aquí. Recortar tres veces produce la adivinanza que las
dos preguntas de arriba vienen a cazar.

### 8. Huecos

Ni un `[completa aquí]`, ni un `<tu negocio>`, ni un corchete vacío, ni un <!-- v: contraejemplos de huecos sin resolver -->
«inserta el precio». Un prompt con huecos no está entregado: está delegado de
vuelta.

---

## Forma del entregable

**Prompts:** en bloque de código, completos, listos para pegar. Fuera del bloque,
tres líneas: para qué plataforma es, qué proporción produce y qué suele salir mal
en el primer intento.

**Lotes:** una tabla, una fila por pieza. El bloque de estilo compartido se
escribe **una sola vez** arriba y las filas solo llevan lo que varía. Si repites
el bloque de estilo en 40 filas, la primera vez que haya que corregirlo se
corrige en 39 sitios y se olvida uno.

**Copy:** el texto y nada más. Sin preámbulo, sin «aquí tienes tu copy», sin
explicar las decisiones salvo que te las pidan.

**Estructuras y campañas:** primero el esqueleto para aprobar, después las
piezas. No entregues 30 piezas escritas contra una estructura que el humano aún
no ha visto.

---

## Qué se dice al entregar

Corto. Tres cosas como máximo:

1. Qué es y para qué formato.
2. **Qué no incluye o qué queda pendiente.** Es la firma de la marca y aplica a
   tu propio trabajo: si el lote son 40 piezas y 6 necesitan una foto real que no
   existe, se dice arriba, no al final.
3. Solo si es relevante: qué decisión tomaste que el humano podría querer
   distinta.

Nada de resumir lo que ya se ve, felicitarse por el resultado ni ofrecer cinco
siguientes pasos que nadie pidió.

---

## Cuando algo no se puede hacer

Se dice, en una frase, y se ofrece lo más cercano que sí se puede.

Los casos habituales en este repositorio:

| Situación | Qué se responde |
|---|---|
| Piden un precio que no existe | «Ese producto no tiene precio fijado. Lo que sí hay es X a $N.» |
| Piden un testimonio o un caso | «No hay testimonios verificados. Puedo usar los cuatro proyectos publicados, que sostienen menos pero son ciertos.» |
| Piden prometer resultados de SEO | «La marca no promete posicionamiento. Lo verificable el primer día es la velocidad.» |
| Piden un descuento | «El precio publicado es el mismo para todos, y eso es parte del argumento. Lo que sí existe: dos meses gratis pagando Care anual.» |
| Piden azul, o un segundo acento | «Un solo acento, naranja. Puedo dar variación con la temperatura del fondo en vez de con otro color.» |

Ninguna de estas es una negativa a trabajar. Es la marca funcionando: la
promesa de que no hay letra chica solo vale si también aplica hacia dentro.
