# Prompts

**Aquí no hay guiones escritos.** No vas a encontrar «el prompt del anuncio de
Start» guardado esperando a ser reutilizado. Lo que hay son **estructuras**: la
anatomía de un prompt PanaClaw, los bloques reutilizables que la componen, y las
variantes por medio y por plataforma.

El prompt se compone cada vez, contra el ADN, para el contexto concreto que pida
el humano. Un prompt guardado envejece en silencio; una estructura no.

---

## Anatomía de un prompt PanaClaw

Seis bloques, siempre en este orden. Los que llevan ★ son obligatorios en
cualquier prompt de imagen o video.

```
1. SUJETO      ★  Qué se ve. Una frase, concreta y física.
2. ESCENA      ★  Dónde está y qué hace la luz.
3. ESTILO      ★  El bloque de marca. Se copia de bloques/estilo-visual.md.
4. ENCUADRE    ★  Proporción, plano, dónde queda el aire para el texto.
5. TEXTO          Solo si la imagen lleva texto dentro. Casi nunca.
6. NEGATIVOS   ★  Lo que no puede aparecer. bloques/negativos.md.
```

**El bloque 3 y el 6 no se improvisan nunca.** Son los que hacen que 40 imágenes
generadas en semanas distintas se vean de la misma marca. Se copian literalmente
de `bloques/`.

---

## Los bloques reutilizables

| Bloque | Qué contiene | Cuándo se usa |
|---|---|---|
| [`bloques/estilo-visual.md`](bloques/estilo-visual.md) | El párrafo de estilo con los hex exactos | Toda imagen y todo video |
| [`bloques/negativos.md`](bloques/negativos.md) | Lo prohibido, en la forma que entiende cada motor | Toda imagen y todo video |
| [`bloques/encuadre.md`](bloques/encuadre.md) | Proporciones por canal y dónde dejar aire | Toda imagen |
| [`bloques/voz.md`](bloques/voz.md) | La voz de la marca comprimida, para pegar en otra IA | Todo prompt de texto |

Un bloque **se copia entero**. No se resume, no se parafrasea y no se «adapta un
poco»: la razón de que existan es que sean idénticos entre piezas.

---

## Por medio

| Archivo | Para qué |
|---|---|
| [`imagen/nano-banana.md`](imagen/nano-banana.md) | Imagen suelta con el modelo de imagen de Gemini |
| [`imagen/lote.md`](imagen/lote.md) | 10, 50 o 200 piezas que tienen que verse hermanas |
| [`video/video-corto.md`](video/video-corto.md) | Reel, story, anuncio en video |
| [`texto/anuncios.md`](texto/anuncios.md) | Copy de pauta |
| [`texto/organico.md`](texto/organico.md) | Publicaciones, WhatsApp, correo |

## Por plataforma

| Archivo | Para qué |
|---|---|
| [`plataformas/pomelli.md`](plataformas/pomelli.md) | Google Labs. **Lleva una advertencia crítica.** |
| [`plataformas/grok.md`](plataformas/grok.md) | Grok, GPT y cualquier modelo ajeno |
| [`plataformas/canva.md`](plataformas/canva.md) | Canva y su IA |

---

## Las cuatro reglas de este directorio

### 1. Un prompt se entrega resuelto

Sin `[tu producto]`, sin `<completa aquí>`, sin corchetes vacíos. Si te falta un
dato para resolverlo —qué producto, qué proporción, qué mensaje— **lo preguntas
antes de generar**. Un prompt con huecos no está entregado: está devuelto.

### 2. Los hex se copian, no se nombran

```
✗  fondo negro con acentos naranja
✓  fondo #100101, acento único #FF5100, brasas #FF1E1E solo en el fondo
```

Los generadores interpretan «naranja» como cualquier cosa entre `#FF8C00` y <!-- v: hex de ejemplo de lo que un generador confunde con naranja -->
`#FF4500`. Con el hex, aciertan mucho más y sobre todo **aciertan igual la <!-- v: hex de ejemplo de lo que un generador confunde con naranja -->
segunda vez**.

### 3. La imagen no lleva el texto

Salvo petición explícita, **el texto va encima en el editor**, no dentro de la
generación. Dos razones: los modelos de imagen siguen escribiendo mal en español
—tildes, eñes, «Ñ» convertida en «N»— y el titular de PanaClaw tiene una
tipografía concreta (Archivo, tracking negativo, versalitas) que ningún generador
reproduce.

Lo que sí se le pide al generador es **dejar el hueco**: aire limpio en el tercio
donde va a caer el titular. Está en `bloques/encuadre.md`.

### 4. Nada de gente

No hay personas en el sistema visual de PanaClaw. Ni clientes sonriendo, ni
equipos en reunión, ni manos sobre teclados. La única excepción tolerada, porque
ya existe en el sitio, es **una mano de cristal oscuro** — que no lee como
humana.

---

## Qué preguntar antes de generar

Tres cosas. Preguntarlas cuesta un mensaje; adivinarlas cuesta rehacer el lote.

1. **Canal y proporción exactos.** «Para Instagram» no basta: feed 1:1, feed 4:5,
   story 9:16 y reel 9:16 no se recortan entre sí sin perder el titular.
2. **Qué producto del catálogo es el sujeto.** Cada uno tiene su escena canónica
   asignada (ver abajo).
3. **Si lleva texto dentro o no.**

---

## Escena canónica por producto

Cada producto tiene ya una imagen asociada en el sitio. Reutilizar la escena
correcta hace que el visitante reconozca el tema sin leer, y que el creativo y la
web se vean del mismo mundo.

| Producto / tema | Escena |
|---|---|
| Velocidad · Sitios web | Proyectil oscuro atravesando estelas de luz roja |
| Seguridad · «que no te lo hackeen» | Monolitos negros con circuitos rojos sobre llanura fracturada |
| Entrega en días | Hélice de bloques de cristal rojo encajados uno tras otro |
| Infraestructura · el sitio es tuyo | Retícula infinita de servidores encendidos en rojo |
| eBot · la máquina que responde | Mano de cristal oscuro tocando una esfera de datos incandescente |
| Proceso · cómo trabajamos | Cintas de luz roja trenzándose sobre obsidiana pulida |
| Start · el punto de partida | Esfera de roca incandescente flotando sola en una cámara oscura |

Las descripciones completas están en
[`adn/03-sistema-visual.md`](../adn/03-sistema-visual.md) y en
[`datos/marca.json`](../datos/marca.json) → `imagen.referenciasDelSitio`.
