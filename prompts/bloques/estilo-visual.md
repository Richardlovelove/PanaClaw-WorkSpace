# Bloque · Estilo visual

El párrafo que hace que una imagen se vea de PanaClaw. **Se copia entero y
literal** en todo prompt de imagen y de video. No se resume ni se parafrasea: su
única razón de existir es ser idéntico entre piezas.

Los hex salen de [`datos/marca.json`](../../datos/marca.json). Si el JSON cambia,
este archivo cambia.

---

## Versión canónica — español

Para Nano Banana, Grok/Aurora y cualquier motor que trabaje bien en español.

```
Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101, casi sin iluminación ambiente. La única luz nace del
propio sujeto: brasas y filamentos incandescentes en naranja #FF5100 y rojo
#FF1E1E. Materiales: obsidiana pulida, cristal negro, roca fundida, metal
oscuro con vetas encendidas. Contraste altísimo, negros profundos que se
tragan los bordes del encuadre, reflejos especulares muy contenidos.
Atmósfera de estudio, aire limpio, sin niebla lechosa. Grano fino de película.
Sin personas.
```

## Versión canónica — inglés

Los motores de imagen siguen entendiendo mejor el inglés. Si el resultado en
español sale flojo, esta es la traducción oficial — **no la reescribas cada vez**.

```
Style: cinematic photography of dark incandescent matter. Warm-black
background #100101 with almost no ambient light. The only light source is the
subject itself: embers and glowing filaments in orange #FF5100 and red
#FF1E1E. Materials: polished obsidian, black glass, molten rock, dark metal
with burning veins. Extreme contrast, deep blacks swallowing the edges of the
frame, tightly controlled specular highlights. Studio atmosphere, clean air,
no milky haze. Fine film grain. No people.
```

---

## Las cinco decisiones que hay dentro

Si tienes que adaptar el bloque a un motor con límite de caracteres, esto es lo
que **no** se puede caer:

1. **`#100101` como fondo.** Negro cálido, no negro puro. Es lo primero que
   identifica a la marca.
2. **La luz nace del sujeto.** No hay lámparas, ni sol, ni luz de ventana. Lo que
   ilumina la escena es lo que está ardiendo dentro de ella. Sin esta frase, los
   motores meten iluminación de estudio convencional y la imagen deja de ser de
   PanaClaw.
3. **Los dos hex de acento**, en ese orden: `#FF5100` primero, `#FF1E1E` después.
4. **Contraste altísimo con negros profundos.** El sujeto tiene que perderse en
   los bordes; es lo que abre el carril para el texto.
5. **`Sin personas` / `No people`.** Va en el bloque de estilo además de en los
   negativos, porque los motores lo ignoran más de la mitad de las veces si solo
   está en un sitio.

---

## Variantes autorizadas

Tres, y solo tres. Cualquier otra variación entra en el bloque de sujeto, no en
el de estilo.

### Frío — para seguridad y auditoría

Sustituye la frase de materiales por:

```
Materiales: obsidiana pulida, cristal negro fracturado, metal oscuro con
circuitos rojos apagándose. La incandescencia es más escasa y más distante.
```

Sigue siendo el mismo mundo, con menos calor. Sirve para el pilar «que no te lo
hackeen», donde una imagen demasiado ardiente lee como celebración.

### Denso — para infraestructura y catálogo

Añade al final:

```
Composición de repetición modular: la misma forma multiplicada hacia el
horizonte, perdiéndose en la oscuridad.
```

Es la escena de la retícula de servidores. Sirve cuando el mensaje es «esto es
un sistema», no «esto es una pieza».

### Íntimo — para eBot y producto

Sustituye «Atmósfera de estudio, aire limpio» por:

```
Plano cercano, profundidad de campo corta, el fondo se disuelve en negro a
pocos centímetros del sujeto.
```

---

## Lo que NO es una variante autorizada

- Cambiar el fondo a claro
- Añadir un segundo color de acento
- Pedir «versión más colorida», «más viva» o «más amigable»
- Añadir personas «solo de fondo»
- Pedir iluminación exterior o luz natural

Si el humano pide alguna de estas, no es una variante de estilo: es otra marca.
Díselo y ofrece la variante autorizada más cercana.
