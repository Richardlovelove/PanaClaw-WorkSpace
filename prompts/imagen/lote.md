# Imagen · Lote

Cómo se generan 10, 50 o 200 piezas que se vean hermanas y no como 200 imágenes
sueltas.

---

## La regla del lote

> **El estilo no varía. El sujeto sí.**

Si varían los dos, no tienes un lote: tienes N imágenes que resultan compartir
paleta. La diferencia se nota inmediatamente en una cuadrícula de Instagram.

En la práctica esto significa que el bloque de estilo y el de negativos **se
escriben una sola vez** y se repiten byte a byte en las N piezas. Lo único que
cambia entre filas es sujeto, escena y encuadre.

---

## Los cuatro ejes de variación

Elige **uno** como eje principal. Como mucho dos. Un lote que varía tres ejes a
la vez se desarma.

| Eje | Varía | Cuándo usarlo |
|---|---|---|
| **Producto** | El sujeto, según la escena canónica de cada producto | Lote de catálogo: una pieza por servicio |
| **Escena** | El mismo tema en siete escenas distintas | Campaña larga sobre un solo producto |
| **Encuadre** | La misma escena en 1:1, 4:5 y 9:16 | Adaptación multicanal de una pieza aprobada |
| **Mensaje** | La imagen es la misma familia; cambia el texto encima | Pruebas A/B de copy |

**El eje de encuadre no cuenta como variación real.** Tres proporciones de la
misma pieza son una pieza, no tres. Cuando el humano pida «40 creativos»,
pregunta si son 40 piezas distintas o 13 piezas en tres formatos.

---

## Formato de entrega

Una tabla. El bloque compartido arriba, escrito **una vez**.

````markdown
## Bloque compartido — se repite idéntico en las 12 piezas

```
Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101 […bloque completo…] Sin personas.

No incluyas: personas, oficinas, laptops ni pantallas; […negativos completos…]
```

## Piezas

| # | Producto | Sujeto + escena | Encuadre |
|---|---|---|---|
| 01 | Start | Una esfera de roca incandescente flotando sola en una cámara vacía de piedra negra. Es pequeña respecto al espacio; la cámara se pierde en la oscuridad a su alrededor. | 4:5, texto abajo |
| 02 | Launch | … | 4:5, texto abajo |
````

**Por qué el bloque va arriba y no repetido en cada fila:** el día que haya que
corregirlo —y lo va a haber— se corrige en un sitio. Repetido en 40 filas se
corrige en 39 y se olvida uno, y esa pieza sale distinta sin que nadie lo note
hasta que está publicada.

---

## Tamaño de lote y variación real

| Piezas | Ejes | Aviso |
|---|---|---|
| 1–6 | Producto o escena | — |
| 7–15 | Producto + escena | Empieza a hacer falta un plan de variación explícito |
| 16–40 | Producto + escena, con encuadres derivados | **Pregunta si son piezas o formatos** |
| 40+ | — | Casi seguro que son menos piezas en más formatos. Aclara antes de producir |

Un lote de 200 piezas visualmente distintas dentro de un sistema tan cerrado
**no existe**. El sistema tiene siete escenas canónicas. Producir 200 obliga o a
romper el estilo o a repetirse; las dos cosas son peores que entregar 20 buenas y
decirlo.

> Si el humano insiste en 200, entrega las 20 piezas madre y las variaciones de
> encuadre y de mensaje que salgan de ellas, y **di explícitamente** cuántas son
> imágenes nuevas y cuántas son derivadas. Es la regla 7: di qué no incluye.

---

## Las siete escenas madre

Todo lote sale de aquí. Están en
[`adn/03-sistema-visual.md`](../../adn/03-sistema-visual.md) y en
[`datos/marca.json`](../../datos/marca.json).

| # | Escena | Significado |
|---|---|---|
| 1 | Proyectil oscuro atravesando estelas de luz roja | Velocidad |
| 2 | Monolitos negros con circuitos rojos sobre llanura fracturada | Seguridad |
| 3 | Hélice de bloques de cristal rojo encajados uno tras otro | Entrega ordenada |
| 4 | Retícula infinita de servidores encendidos hacia el horizonte | Infraestructura |
| 5 | Mano de cristal oscuro tocando una esfera de datos | La máquina que responde |
| 6 | Cintas de luz roja trenzándose sobre obsidiana pulida | Proceso |
| 7 | Esfera de roca incandescente sola en una cámara oscura | Punto de partida |

### Cómo se saca variación sin romper el sistema

De cada escena madre salen entre tres y cinco piezas variando **una** de estas:

- **Distancia:** plano general → plano medio → macro del detalle incandescente
- **Ángulo:** frontal → picado → contrapicado → lateral
- **Cantidad:** un objeto → tres → una multitud que se pierde
- **Momento:** encendiéndose → en pleno brillo → apagándose

Cuatro dimensiones × siete escenas ya da margen de sobra para cualquier campaña
real, y todo sigue siendo la misma marca.

---

## Control de calidad del lote

No revises pieza a pieza. Revisa **en cuadrícula**, que es como se van a ver.

1. **Monta las N en una rejilla.** Si una salta a la vista, está mal aunque
   suelta sea buena.
2. **Comprueba la temperatura.** El fallo más común de un lote es que algunas
   piezas se fueron a amarillo y otras a rojo. Todas tienen que compartir el
   mismo `#FF5100`.
3. **Comprueba los huecos.** El motor deja detalle en la zona limpia una de cada
   tres veces. En un lote de 30, eso son diez piezas que no admiten titular.
4. **Recorta todo a 1:1** mentalmente. Alguna red lo va a hacer.
5. **Cuenta las personas.** Debería salir cero. Si en 30 piezas hay una silueta,
   se regenera esa.

---

## Qué se entrega con el lote

- La tabla con las N piezas resueltas
- El bloque compartido, una vez
- **Cuántas son piezas nuevas y cuántas son derivadas de encuadre**
- Qué piezas necesitan algo que no existe (una foto real, un dato sin verificar)
  y por tanto no se pueden producir

Lo último es obligatorio. Un lote entregado como «40 listas» cuando seis dependen
de material inexistente es exactamente la letra chica que la marca dice no tener.
