# Video corto

Reel, story y anuncio en video. Estructura plano a plano, no guion escrito.

---

## Antes de empezar: tres preguntas

1. **Duración.** 6 s (anuncio), 15 s (story), 20–30 s (reel).
2. **¿Lleva voz?** La marca **no tiene locutor definido**. Si hace falta voz,
   se pregunta: ¿voz del dueño, voz sintética, o solo texto en pantalla?
3. **La única acción que tiene que provocar.** Un video con dos llamadas no tiene
   dos: tiene cero.

Por defecto, si no te dicen otra cosa: **sin voz, texto en pantalla, 15 s**.

---

## La estructura de tres tiempos

Es la del sitio, comprimida. Funciona en las tres duraciones.

```
1. EL DESASTRE   40 %   Lo que le pasa hoy al que mira. Concreto, sin dramatizar.
2. LA CIFRA      35 %   El precio o el plazo. Desnudo, sin adornos.
3. LA SALIDA     25 %   Una sola acción.
```

**El primer plano no es la marca.** Es el problema. Un video que abre con el logo
pierde a quien está deslizando, y la marca es exactamente lo que todavía no le
importa a nadie.

---

## Reparto por duración

### 6 segundos — anuncio

| Tiempo | Qué se ve | Texto |
|---|---|---|
| 0–2,5 s | Escena madre, plano cerrado, movimiento continuo | El desastre, 4–6 palabras |
| 2,5–5 s | La misma escena abriéndose | La cifra, sola y grande |
| 5–6 s | Negro con el símbolo y el wordmark | El CTA |

### 15 segundos — story

| Tiempo | Qué se ve | Texto |
|---|---|---|
| 0–1 s | Negro. Un filamento encendiéndose | — |
| 1–6 s | Escena madre, plano general lento | El desastre, en dos líneas |
| 6–11 s | Corte a plano cerrado del detalle incandescente | La cifra + el plazo |
| 11–14 s | La escena apagándose | Qué NO incluye, en una línea |
| 14–15 s | Negro, símbolo, wordmark | El CTA |

> El plano de «qué no incluye» es el que distingue un video de PanaClaw de
> cualquier otro anuncio. No lo cortes por falta de tiempo: corta antes el plano
> de apertura.

### 25 segundos — reel

Igual que el de 15, con un tiempo más entre la cifra y el cierre: **la objeción**.
Cinco segundos que nombran lo que el espectador está pensando y lo contestan.

---

## Prompt de generación de video

Si el video es sintético (Veo, Sora o similar), un plano = un prompt. La misma
anatomía que en imagen, más el movimiento.

```
[SUJETO Y ESCENA, una frase]

[MOVIMIENTO: qué se mueve y qué hace la cámara. Una sola cosa.]

Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101, casi sin iluminación ambiente. La única luz nace del
propio sujeto: brasas y filamentos incandescentes en naranja #FF5100 y rojo
#FF1E1E. Materiales: obsidiana pulida, cristal negro, roca fundida, metal
oscuro con vetas encendidas. Contraste altísimo, negros profundos que se
tragan los bordes del encuadre. Grano fino de película. Sin personas.

Cámara: [un solo movimiento lento]. Duración [N] segundos. Composición
vertical 9:16, el tercio inferior en negro limpio para el texto.

No incluyas: personas, oficinas, laptops ni pantallas; ningún azul, verde,
morado ni tono pastel; nada de blanco puro ni fondos claros; nada de luz
natural ni exteriores; ningún texto, letra ni número; nada de estética de
stock corporativo.
```

### Ejemplo — plano de velocidad, 4 s

```
Un proyectil de obsidiana pulida atravesando el cuadro, dejando estelas de luz
que se estiran detrás de él.

Movimiento: el proyectil cruza de derecha a izquierda a velocidad constante;
las estelas se alargan y se apagan a su paso. Nada más se mueve.

Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101, casi sin iluminación ambiente. La única luz nace del
propio sujeto: brasas y filamentos incandescentes en naranja #FF5100 y rojo
#FF1E1E. Materiales: obsidiana pulida, cristal negro, roca fundida, metal
oscuro con vetas encendidas. Contraste altísimo, negros profundos que se
tragan los bordes del encuadre. Grano fino de película. Sin personas.

Cámara: fija, sin movimiento. Duración 4 segundos. Composición vertical 9:16,
el tercio inferior en negro limpio para el texto.

No incluyas: personas, oficinas, laptops ni pantallas; ningún azul, verde,
morado ni tono pastel; nada de blanco puro ni fondos claros; nada de luz
natural ni exteriores; ningún texto, letra ni número; nada de estética de
stock corporativo.
```

---

## Reglas de movimiento

Heredadas del sitio, y no son cosméticas:

- **Un solo movimiento por plano.** O se mueve el sujeto o se mueve la cámara.
  Nunca los dos.
- **Lento.** Ningún movimiento de cámara rápido, ningún zoom brusco, ningún
  latigazo. El sistema visual es denso y oscuro: el movimiento rápido lo
  convierte en ruido.
- **Sin transiciones de efecto.** Corte seco o fundido a negro. Nada de barridos,
  giros ni desenfoques de transición.
- **Cortes largos.** Mínimo 2 s por plano en un video de 15 s. Un montaje picado
  es de otra marca.

---

## Texto en pantalla

- **Archivo.** Titular peso 600, versalitas, tracking `-0.02em`, `#FFF7F7`.
- **Entra por opacidad**, no deslizándose. Si algo se mueve, es la imagen.
- **Una idea por plano.** Si no cabe en dos líneas, sobra la mitad.
- **Nunca en `#FF1E1E`.** El ember es color de fondo. El acento de texto es
  `#FF5100` y se reserva para la cifra o el antetítulo.
- **La cifra va sola en su plano.** `$295` ocupando la pantalla hace más trabajo
  que cualquier frase.

---

## Sonido

No hay identidad sonora definida. Hasta que la haya:

- Reel y story se consumen sin sonido la mayoría de las veces → **el video tiene
  que funcionar mudo**. Si depende del audio para entenderse, está mal montado.
- Si se pone música, instrumental y grave, sin voz, sin percusión marcada.
- **Sin efectos de sonido de interfaz** —clics, whooshes, notificaciones—. Son de
  otra categoría de anuncio.

---

## Antes de publicar

- [ ] ¿Se entiende sin sonido?
- [ ] ¿El primer plano es el problema, no la marca?
- [ ] ¿Hay una sola llamada a la acción?
- [ ] ¿Está el plano de «qué no incluye»?
- [ ] ¿La cifra coincide con `datos/precios.json`?
- [ ] ¿Algún texto en `#FF1E1E`? → cámbialo
- [ ] ¿Se lee el texto dentro de las zonas seguras de story?
