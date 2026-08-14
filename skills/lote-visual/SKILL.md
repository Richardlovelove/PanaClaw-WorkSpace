# Skill · Lote visual

Produce N prompts de imagen que generan piezas hermanas: mismo sistema visual,
sujetos distintos.

---

## 1 · Cuándo se usa

**Se dispara con:**
- «Genera 20 creativos»
- «Un lote de imágenes para todo el mes»
- «Variaciones de esta pieza»
- «Necesito los creativos de la campaña»

**NO se usa cuando:**
- Piden **una** imagen → [`prompts/imagen/nano-banana.md`](../../prompts/imagen/nano-banana.md) directamente
- Piden video → [`prompts/video/video-corto.md`](../../prompts/video/video-corto.md)
- Piden el copy, no la imagen → [`anuncio-pagado`](../anuncio-pagado/SKILL.md)

---

## 2 · Qué se lee

1. [`datos/marca.json`](../../datos/marca.json) — los hex exactos
2. [`prompts/README.md`](../../prompts/README.md) — la anatomía y la tabla de
   escena canónica por producto
3. [`prompts/bloques/estilo-visual.md`](../../prompts/bloques/estilo-visual.md) — el bloque compartido
4. [`prompts/bloques/negativos.md`](../../prompts/bloques/negativos.md)
5. [`prompts/bloques/encuadre.md`](../../prompts/bloques/encuadre.md)
6. [`prompts/imagen/lote.md`](../../prompts/imagen/lote.md) — la regla del lote

---

## 3 · Qué se pregunta antes de empezar

1. **¿Cuántas piezas y en cuántas proporciones?** No es lo mismo 40 piezas que 13
   piezas en tres formatos. Si dicen «40 creativos», **pregunta cuál de las dos**.
2. **¿Qué eje varía: producto, escena, encuadre o mensaje?**
3. **¿Llevan texto dentro de la imagen?**

**Por defecto**, si dicen «lo que veas»:
- Eje: producto
- Proporción: 4:5 (feed) + 9:16 (story)
- Texto dentro: no

---

## 4 · Procedimiento

### Paso 1 · Decidir el eje

Uno principal, dos como máximo. Los cuatro ejes están en
[`prompts/imagen/lote.md`](../../prompts/imagen/lote.md).

**Si varían tres ejes, el lote se desarma.** Reduce y dilo.

### Paso 2 · Comprobar que el número es realista

El sistema tiene **siete escenas madre**. De cada una salen 3–5 piezas variando
distancia, ángulo, cantidad o momento: unas **20–35 piezas reales** como techo.

Por encima de eso, o se rompe el estilo o se repite. Si piden más:
entrega las piezas madre + las derivadas de encuadre, y **di cuántas son nuevas y
cuántas derivadas**.

### Paso 3 · Escribir el bloque compartido, una vez

Copia literal de estilo + negativos. **No lo repitas en cada fila**: el día que
haya que corregirlo se corrige en 39 sitios y se olvida uno.

### Paso 4 · Resolver cada pieza

Por fila: producto, sujeto + escena, encuadre. Nada más — el estilo ya está
arriba.

Usa la tabla de escena canónica de
[`prompts/README.md`](../../prompts/README.md): cada producto tiene la suya, y
respetarla hace que el creativo y la web se vean del mismo mundo.

### Paso 5 · Añadir los negativos específicos

Algunos temas necesitan negativos extra:

| Tema | Añadir a negativos |
|---|---|
| Seguridad | `candados, escudos, iconos de seguridad` |
| eBot | `robots, androides, burbujas de chat` |
| Tienda / Commerce | `carritos de compra, bolsas, iconos de tienda` |

### Paso 6 · Entregar

Tabla, bloque compartido arriba, y el recuento de nuevas vs. derivadas.

---

## 5 · Verificación

- [ ] ¿El bloque de estilo está **una sola vez** y es idéntico para todas?
- [ ] ¿Todo hex sale de [`datos/marca.json`](../../datos/marca.json)?
- [ ] ¿Cada pieza tiene su encuadre con el hueco descrito como «negro limpio», no
      como «espacio para el texto»?
- [ ] ¿Varía un solo eje principal?
- [ ] ¿Cada tema lleva sus negativos específicos?
- [ ] ¿Está el recuento de piezas nuevas vs. derivadas?
- [ ] ¿Alguna pieza depende de material que no existe? → dilo
- [ ] ¿Huecos sin resolver en algún prompt?

**Después de generar las imágenes** (esto lo hace quien las genera, no el agente):

- [ ] Míralas **en cuadrícula**, no una a una. Si alguna salta, está mal
- [ ] ¿Todas comparten la misma temperatura de naranja?
- [ ] ¿Los huecos están realmente limpios? Falla ~1 de cada 3
- [ ] ¿Cero personas?

---

## Qué se dice al entregar

1. Cuántas piezas, en qué proporciones, para qué canal
2. **Cuántas son imágenes nuevas y cuántas derivadas de encuadre**
3. Qué piezas no se pueden producir y por qué
