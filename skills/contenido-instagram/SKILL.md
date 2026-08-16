# Skill · Contenido de Instagram

Produce **un solo prompt maestro, listo para pegar en Meta AI**, que devuelve un
documento HTML con el mes entero: las piezas ya compuestas con su texto, la
descripción de cada publicación, sus hashtags y el botón para descargarlas en
PNG a 1080×1350.

---

## 1 · Cuándo se usa

**Se dispara con:**
- «Dame el contenido de Instagram del mes»
- «Planeamiento de contenido para el siguiente mes, enfocado en eBot»
- «Necesito las publicaciones del mes con sus descripciones»
- «El prompt para que Meta me arme las piezas»

**NO se usa cuando:**
- Piden **una** pieza suelta → [`prompts/imagen/nano-banana.md`](../../prompts/imagen/nano-banana.md)
- Piden solo los fondos, sin texto ni descripciones → [`lote-visual`](../lote-visual/SKILL.md)
- Piden **pauta**, no orgánico → [`anuncio-pagado`](../anuncio-pagado/SKILL.md)
- Piden la campaña completa con embudo y presupuesto → [`campanas/README.md`](../../campanas/README.md)
  primero, y esta skill después para la parte orgánica

---

## 2 · Qué se lee

En este orden:

1. [`datos/precios.json`](../../datos/precios.json) — toda cifra que se vaya a decir
2. [`datos/marca.json`](../../datos/marca.json) → `redesSociales` — retícula, escala, velo
3. [`adn/02-voz-y-tono.md`](../../adn/02-voz-y-tono.md) — y en particular «La excepción de redes sociales»
4. [`adn/04-audiencia.md`](../../adn/04-audiencia.md) — el público del mes y sus objeciones
5. [`catalogo/`](../../catalogo/) — la ficha del producto del mes, entera
6. [`catalogo/08-fronteras.md`](../../catalogo/08-fronteras.md) — si el mes toca Care, Seguridad, Diagnóstico o Auditoría
7. [`prompts/texto/organico.md`](../../prompts/texto/organico.md) — los cinco tipos de publicación
8. [`prompts/imagen/texto-en-imagen.md`](../../prompts/imagen/texto-en-imagen.md) — la maquetación
9. [`prompts/plataformas/meta-ai.md`](../../prompts/plataformas/meta-ai.md) — el contrato
10. [`campanas/plantillas/calendario.md`](../../campanas/plantillas/calendario.md) — la mezcla de tipos
11. [`prompts/bloques/estilo-visual.md`](../../prompts/bloques/estilo-visual.md) y
    [`negativos.md`](../../prompts/bloques/negativos.md) — se copian literales

---

## 3 · Qué se pregunta antes de empezar

1. **¿Qué producto es el foco del mes?** Cambia el público, las objeciones y las
   escenas. Un mes es de un producto, no de seis.
2. **¿Cuántas publicaciones?**
3. **¿Hay algo del mes anterior que no se pueda repetir?**

Si el humano ya los dio, no preguntes nada y produce.

**Valores por defecto**, si dice «lo que veas»:
- Publicaciones → **12**
- Formato → todo 4:5, 1080×1350
- Carruseles → entre 4 y 6 del total; el resto piezas sueltas
- Llamada a la acción → en 4 de 12, nunca más

---

## 4 · Procedimiento

### Paso 1 · Fijar el público, el ángulo y la firma

Del producto sale el público, y de
[`adn/04-audiencia.md`](../../adn/04-audiencia.md) salen su situación, lo que
teme y su objeción principal. **Un solo público y un solo ángulo en el mes.**

Y la firma, que también la manda el producto: la tagline de su ficha de
[`catalogo/`](../../catalogo/) si tiene una declarada, y la de marca si no. La
tabla está en [`adn/02-voz-y-tono.md`](../../adn/02-voz-y-tono.md). Se fija aquí
y no cambia en las doce.

Escríbelos antes de nada. Todo lo demás se mide contra ellos: una publicación que
no le habla a ese público sobra aunque esté bien escrita.

### Paso 2 · Repartir los tipos

Los cinco tipos están en
[`prompts/texto/organico.md`](../../prompts/texto/organico.md). Para doce
publicaciones, esta mezcla funciona:

| Tipo | Cuántas |
|---|---|
| Cifra publicada | 4 |
| Desastre explicado | 3 |
| Objeción contestada | 3 |
| Frontera | 1 |
| Trabajo enseñado | 1 |

**El «trabajo enseñado» solo entra si hay un proyecto publicado y verificado que
encaje.** Si no lo hay, se sustituye por otra cifra publicada y **se dice al
entregar** — no se rellena con un caso inventado.

### Paso 3 · Escribir el texto de cada pieza

Por publicación, y en este orden:

1. **El titular**, que es lo que va dentro de la imagen. La situación primero,
   nunca el nombre del plan. De 2 a 8 líneas, con los cortes ya decididos y el
   tramo naranja ya marcado, según
   [`prompts/imagen/texto-en-imagen.md`](../../prompts/imagen/texto-en-imagen.md).
2. **La descripción**, con las tres articulaciones y su firma al cierre.
3. **Los hashtags**, seis como máximo.
4. **La nota del límite**, si la pieza dice una cifra o un plazo. Obligatoria.

**Toda cifra se copia de [`datos/precios.json`](../../datos/precios.json) en el
momento de escribirla**, no de memoria. Y un importe único no se suma nunca a uno
mensual: eBot es `$499` de una vez, y aparte los `$5` al mes de la nube y los
`$1–2` al mes de la llave de inteligencia artificial.

### Paso 4 · Asignar la escena a cada pieza

La tabla de escena canónica por producto está en
[`prompts/README.md`](../../prompts/README.md). Se respeta: es lo que hace que el
visitante reconozca el tema sin leer.

Dentro de la escena madre se varía distancia, ángulo, cantidad o momento. **El
bloque de estilo no varía nunca** — si varían el estilo y el sujeto a la vez, no
es un mes de contenido, son doce imágenes sueltas.

Y los negativos específicos del tema, de
[`skills/lote-visual/SKILL.md`](../lote-visual/SKILL.md) paso 5. Para eBot:
`robots, androides, burbujas de chat`.

### Paso 5 · Elegir anclaje y tamaño por pieza

Mecánico, no artístico: el número de líneas del titular decide el tamaño, y el
tamaño decide el anclaje. La tabla está en
[`prompts/imagen/texto-en-imagen.md`](../../prompts/imagen/texto-en-imagen.md).

El anclaje decide dónde tiene que quedar limpio el fondo, y eso se escribe dentro
del prompt de esa pieza — describiendo **qué hay** en esa zona (negro limpio, la
incandescencia apagándose), nunca «espacio para el texto».

### Paso 6 · Armar el prompt maestro

Siete secciones, en este orden. El orden no es decorativo: la prohibición de
escribir va primero y se repite al final, porque en un prompt largo una sola
mención se le olvida a la mitad.

```
━━ 1. QUÉ ERES Y QUÉ NO HACES ━━
El reparto del trabajo y la prohibición literal de redactar, mejorar,
acortar, traducir o completar cualquier texto.

━━ 2. EL SISTEMA VISUAL ━━
Los cinco hex. Las dos familias con sus roles. La retícula en píxeles. La
escala completa. El velo. La regla del acento naranja.

━━ 3. EL CONTRATO DEL HTML ━━
Las dos fuentes de Google Fonts. Lienzo de 1080×1350 exactos. Botón de
descarga por pieza y botón de descargar todas. Descripción y hashtags en
texto seleccionable debajo de cada pieza.

━━ 4. EL BLOQUE DE ESTILO ━━
Literal, de prompts/bloques/estilo-visual.md. Una sola vez.

━━ 5. LOS NEGATIVOS ━━
Literal, de prompts/bloques/negativos.md, más los del tema del mes.

━━ 6. LAS PIEZAS ━━
Una por una: número, tipo, titular con sus cortes y su tramo naranja,
anclaje, prompt del fondo, descripción, hashtags.

━━ 7. ANTES DE DEVOLVER ━━
La lista que Meta tiene que comprobar, con la prohibición repetida.
```

### Paso 7 · Entregar

El prompt maestro completo, en un bloque, listo para pegar. Ver
[`orquestador/protocolo-entrega.md`](../../orquestador/protocolo-entrega.md).

---

## 5 · Verificación

Antes de entregar, una a una:

- [ ] ¿Toda cifra existe en [`datos/precios.json`](../../datos/precios.json)?
- [ ] ¿Todo hex sale de [`datos/marca.json`](../../datos/marca.json)?
- [ ] ¿Algún pago único sumado a una mensualidad?
- [ ] ¿Algún rango citado por su mínimo a secas, sin «desde»?
- [ ] ¿Jerga? Búsqueda literal, no de memoria
- [ ] ¿Algún dato, métrica, testimonio o proceso que no exista en el catálogo?
- [ ] ¿Cada pieza que dice una cifra o un plazo lleva su nota de límite?
- [ ] ¿Un solo público y un solo ángulo en las doce?
- [ ] ¿Llamada a la acción en 4 como mucho?
- [ ] ¿Seis hashtags o menos en todas, y todos concretos?
- [ ] ¿Emojis solo en las descripciones, y solo en sus tres articulaciones?
- [ ] ¿Ninguna descripción sin su firma al cierre, y la misma en las doce?
- [ ] ¿La firma es la tagline del producto del mes, y no una inventada?
- [ ] ¿Alguna pieza dice su tagline tres veces —titular, apertura y firma—?
- [ ] ¿Cada titular cabe en 8 líneas, con los cortes escritos?
- [ ] ¿Un solo tramo naranja por titular?
- [ ] ¿El bloque de estilo está una sola vez y es idéntico para todas?
- [ ] ¿La prohibición de escribir aparece al principio **y** al final?
- [ ] ¿Huecos sin resolver en el prompt maestro?

---

## Qué se dice al entregar

Tres cosas como máximo:

1. Cuántas publicaciones, de qué producto, para qué público y en qué formato.
2. **Qué no incluye:** qué pieza no se pudo escribir por falta de material
   verificado, y qué dato haría falta para completarla.
3. Solo si aplica: qué decisión tomaste que el humano podría querer distinta.
