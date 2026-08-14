# Sistema visual

La versión legible de [`datos/marca.json`](../datos/marca.json), con el porqué de
cada decisión. **Los valores exactos se copian del JSON, no de aquí** — este
archivo explica, el JSON manda.

---

## La imagen mental

PanaClaw se ve como **materia oscura incandescente**. Obsidiana, cristal negro,
roca fundida, circuitos rojos, estelas de luz a alta velocidad. Un mundo casi
negro donde algo está ardiendo justo fuera de plano.

No se ve como: una oficina, un equipo sonriendo, un portátil sobre un escritorio
de madera clara, una ilustración plana de personajes, un degradado azul-morado,
un gráfico de barras subiendo.

La razón es de posicionamiento, no de gusto. Toda agencia web del mercado usa
azul, blanco y fotos de stock de gente reunida. PanaClaw se define contra esa
categoría, y el color es lo primero que lo comunica —antes de que nadie lea una
palabra.

---

## Color

### La paleta

| Token | Hex | Para qué |
|---|---|---|
| `deep-black` | `#100101` | Fondo maestro de todo |
| `flash-orange` | `#FF5100` | **El único acento.** UI, texto de acento, viñetas |
| `ember-red` | `#FF1E1E` | **Solo fondos.** Degradados, vetas, atmósfera |
| `signal-red` | `#EE0000` | Paso intermedio en degradados. No se usa suelto |
| `soft-white` | `#FFF7F7` | Texto principal |
| `studio-gray` | `#BABABA` | Texto secundario, bajadas, notas |

### Las dos reglas de color

**1. Un solo acento.** Naranja para todo lo que destaca. Añadir un segundo color
de acento es la forma más rápida de que la marca deje de reconocerse.

**2. El ember nunca toca un texto.** `#FF1E1E` existe para el shader del hero,
para las vetas de las imágenes y para los degradados de fondo. En cuanto aparece
en una letra, el naranja deja de ser el acento y hay dos rojos peleando.

### Detalles que importan

El negro **no es negro puro**: `#100101` lleva un punto de rojo. El blanco
**no es blanco puro**: `#FFF7F7` es cálido. Puestos uno al lado del otro con sus
versiones puras la diferencia es sutil; en una pantalla entera es lo que separa
«marca» de «plantilla».

Los fondos de tarjeta son `rgba(255,255,255,.02)` con borde
`rgba(255,255,255,.10)`. Una tarjeta de PanaClaw es un rectángulo de vidrio
**apenas** más claro que el fondo, nunca una caja blanca ni gris.

### Prohibido

Azul de cualquier tono · verde · morado · amarillo · pasteles · `#FFFFFF` puro ·
`#000000` puro · degradados multicolor · un segundo acento.

### Deuda conocida

Blanco sobre naranja da 3.1:1 de contraste y WCAG AA pide 4.5:1 a ese cuerpo de
letra. Es una decisión de marca tomada a sabiendas y anotada en el CSS del sitio:
cumplirla con blanco exigiría bajar el naranja a ~`#D64200`, que ya es tocar el <!-- v: hex de ejemplo: lo que costaría cumplir AA, no es token de marca -->
acento. **No lo «arregles» por tu cuenta.**

---

## Tipografía

**Archivo. Una sola familia, para todo.** No hay serif de titulares, no hay fuente
display, no hay segunda familia. Pesos en uso: 300, 400, 500, 600, 700.

### La firma tipográfica

Tres elementos, y juntos identifican a la marca sin logo:

1. **Titular en versalitas apretadas.** `uppercase`, peso 600, interlínea 0.98
   (menos que 1 — las líneas casi se tocan), tracking negativo `-0.02em`, ancho
   máximo 14 caracteres. El titular es un bloque compacto, no una línea suelta.
2. **Antetítulo naranja espaciado.** 14px, `uppercase`, tracking `0.16em`, color
   `#FF5100`. Va encima del titular y es lo más reconocible del sistema.
3. **Bajada gris y ligera.** 18px, peso **300**, color `#BABABA`, máximo 52
   caracteres de ancho. El contraste de peso entre el 600 del titular y el 300 de
   la bajada es deliberado.

### Escala

| Rol | Tamaño | Peso |
|---|---|---|
| H1 hero | `clamp(48px, 8vw, 112px)` | 600 |
| H2 sección | `clamp(36px, 5vw, 64px)` | 600 |
| Antetítulo | 14px, tracking .16em | 400 |
| Bajada | 18px | 300 |
| Cuerpo | 15–17px, interlínea 1.6 | 300 |
| Precio | 44px, tracking -.02em | 600 |
| Botón | 13–14px, tracking .03–.06em | 500 |
| Wordmark | tracking .20em, uppercase | 700 |

> **Escribe en minúscula.** Las mayúsculas las pone el CSS. Un texto entregado ya
> gritado no se puede volver a bajar.

---

## Forma

- **Píldora `999px`** — nav, botones, badges, chips. La forma más frecuente.
- **Tarjeta `20–22px`** — planes, servicios, care.
- **Campo `12px`** — inputs, selects.
- **Icono, 22 % del lado** — favicon.

**Bordes:** 1px `rgba(255,255,255,.10)`.
**Sombras:** `0 14px 48px rgba(0,0,0,.55)`. Profundas y difusas, nunca duras ni
con desplazamiento lateral.
**Cristal:** `backdrop-filter: blur(26px) saturate(150%)` sobre `rgba(9,1,1,.88)`.
Es el tratamiento del nav flotante y el efecto más caro de imitar mal.
**Viñeta de lista:** punto naranja de 8px. **Nunca un check verde**, nunca un
guion.

---

## Imágenes

> **Las imágenes van de fondo, nunca como pieza de producto.** A sangre,
> apagadas y bajo un velo que abre carril al texto. Lo que brilla es el titular.

Es la regla 9 del repositorio del sitio y define todo el tratamiento fotográfico:

- Origen 16:9, recorte con `object-position` decidido por escena
- Opacidad 0.4–0.5 por defecto; hasta 0.85 en imágenes muy oscuras que si no
  desaparecen
- Sin personas, sin oficinas, sin manos sobre teclados, sin stock corporativo
- Una excepción tolerada: manos **de cristal oscuro**, no humanas

### Las siete escenas canónicas

Son las que ya usa el sitio. Sirven de referencia directa para cualquier
generador de imagen:

1. Proyectil oscuro atravesando estelas de luz roja a alta velocidad
2. Monolitos negros con circuitos rojos sobre una llanura fracturada
3. Hélice de bloques de cristal rojo encajados uno tras otro
4. Retícula infinita de servidores encendidos en rojo hacia el horizonte
5. Una mano de cristal oscuro tocando una esfera de datos incandescente
6. Cintas de luz roja trenzándose sobre obsidiana pulida
7. Esfera de roca incandescente flotando sola en una cámara oscura

Cada una está atada a un significado: velocidad, seguridad, entrega ordenada,
infraestructura, la máquina que responde, el proceso, el punto de partida.
Reutilizar la escena correcta hace que el visitante reconozca el tema sin leer.

---

## Movimiento

- **Sin librería de animación.** Solo transiciones CSS; el JavaScript únicamente
  decide cuándo dispararlas.
- **Solo `transform` y `opacity`.** Cualquier otra propiedad provoca repintados,
  y el argumento entero de la marca es la velocidad.
- **0.2–0.3s, ease.** Nada por encima de 0.35s.
- **`prefers-reduced-motion: reduce` apaga todo.** Sin excepción.

Aquí vivió GSAP: pesaba 43 KB comprimidos, el 74 % de todo el JavaScript del
sitio, y lo único que hacía era poner un atributo cuando un elemento entraba en
pantalla. En una página que vende abrir en menos de un segundo, eso no se
sostiene.

---

## Logo

**Símbolo:** un rayo sobre cuadrado negro, con degradado `#FF5100` → `#FF1E1E`.

```
path:    M37.5 6 18 35.5h11.2L26.5 58 46 28.5H34.8L37.5 6Z
viewBox: 0 0 64 64
fondo:   #100101, esquinas al 22 %
```

**Wordmark:** `PANACLAW` en Archivo 700, tracking `0.20em`, `#FFF7F7`, seguido de
un punto `.` en `#FF5100`. El punto naranja es parte de la marca.

**Prohibido:** rayo en otro color, rayo sobre fondo claro, estirar/rotar/inclinar,
wordmark sin tracking, y cualquier efecto añadido (sombra, contorno, bisel,
brillo).

**Regenerar:** `npm run brand` en el repositorio del sitio. Los favicons y el
`og.png` son archivos generados que **no** se recalculan en cada build; hay que
correr el script y commitear lo que cambie.

---

## Layout

Contenedor `max-width: 1280px`, padding lateral 40px (24px en móvil). Secciones
con 120px de padding vertical. Rejillas de 3 columnas para servicios y
capacidades, 4 para planes, gap 18–24px.

**Una sola fuente de verdad para cada medida.** Dos reglas calculando el mismo
ancho es el bug que más ha costado en el repositorio del sitio: pasó con el
navbar y con el panel del chat, y las dos veces se veía bien en escritorio y roto
en teléfono.
