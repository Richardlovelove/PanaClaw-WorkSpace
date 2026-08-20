# Texto · Blog

Estructura de un post del blog de PanaClaw. Es el único formato orgánico que se
escribe para Google antes que para nadie, y el único que tiene un contrato
técnico que no se puede romper sin que falle el `build` del sitio.

**Base obligatoria:** [`adn/02-voz-y-tono.md`](../../adn/02-voz-y-tono.md),
[`adn/06-claridad.md`](../../adn/06-claridad.md) y
[`adn/07-redaccion.md`](../../adn/07-redaccion.md). El segundo decide por dónde
empieza el post — la consecuencia, nunca el precio ni el límite —, y el tercero
decide si además se lee entero. Para el procedimiento completo, con el orden de
lectura y la verificación, usa [`skills/blog-seo/SKILL.md`](../../skills/blog-seo/SKILL.md).

---

## Qué distingue el blog de todo lo demás en `prompts/texto/`

[`organico.md`](organico.md) se escribe para alguien que ya está mirando el
perfil. El blog se escribe para alguien que **todavía no sabe que PanaClaw
existe** y escribió una pregunta en Google. Eso cambia dos cosas:

1. **El titular no es un gancho de marca, es una respuesta a una búsqueda
   real.** «Cuánto cuesta una página web en Panamá», no «Por qué tu web tarda
   una eternidad». La persona que busca lo primero no está pensando en
   PanaClaw todavía; la que busca lo segundo, tampoco — pero solo la primera
   frase es lo que alguien escribe en la caja de Google.
2. **El post no vende en el cuerpo.** Vende en el título de Google, en el
   enlace interno del cierre y en la tarjeta de conversión que pone la propia
   plantilla del sitio al final de cada post — automática, no se redacta.
   Meter una llamada a la acción a mitad del texto interrumpe a quien todavía
   está leyendo para entender.

---

## El contrato técnico

Es un espejo del schema real, en
`abrinay1997-stack/PanaClaw` → `src/content.config.ts`. **Ahí es un `zod.object()`
que hace fallar el `build` si un campo no cumple**, así que esto no es una
sugerencia de estilo: es lo que exige el código para publicar.

```yaml
---
title: "…"          # 15–90 caracteres. El <h1> y el <title> de la pestaña.
description: "…"    # 60–200 caracteres. El resumen del listado y la meta description.
date: AAAA-MM-DD     # Fecha de publicación. Ordena el listado.
category: …          # Uno de los cinco de la tabla de abajo. Ninguno más.
keywords: […, …]     # 1 a 6. Deciden qué posts salen como «relacionados».
readingTime: N        # Entero, 2 a 30. Minutos, a ojo de quien lo escribió.
draft: false          # Opcional, por defecto false. true = no sale en el listado.
---
```

**Si un dato no cumple el rango, el post no se entrega así.** Se corrige antes,
no se deja para que lo note quien lo publique.

### Las cinco categorías, y solo estas

| Categoría | Se usa para | Ejemplo ya publicado |
|---|---|---|
| `precios` | Cuánto cuesta algo, y por qué | «Cuánto cuesta una página web en Panamá» |
| `guias` | Cómo decidir, cómo elegir, qué preguntar | «Cómo elegir agencia web: 9 preguntas» |
| `comparativas` | Una opción contra otra, sin bando | «WordPress vs. sitio a medida» |
| `casos` | Un proyecto propio, contado | Ninguno todavía — ver «Lo que hoy no se puede escribir» |
| `panama` | Contexto local: Yappy, ley de datos, mercado panameño | — |

**Añadir una sexta categoría no es una decisión de contenido.** Hay que tocar
el enum de `src/content.config.ts` en el otro repositorio y el mapa de
etiquetas de `src/pages/blog/index.astro` y `[slug].astro`. Si un tema no
encaja en las cinco, se dice y se pregunta antes de forzarlo en la que más se
parece.

### El slug

El nombre del archivo, sin extensión, es la URL: `src/content/blog/como-elegir-agencia-web-panama.md`
→ `panaclaw.com/blog/como-elegir-agencia-web-panama/`. Reglas:

- Minúsculas, guiones, sin acentos ni eñes.
- Describe el tema en 3 a 6 palabras, no repite el título entero.
- **No puede repetir uno que ya exista.** Antes de proponerlo, se comprueba
  contra `src/content/blog/` del repositorio del sitio.

---

## Anatomía del cuerpo

```
LEAD        1–2 párrafos. La escena o la pregunta, a la altura de la
            consecuencia — nunca abre con el precio ni con la marca.
H2 × 4–8    Un subtema por encabezado. Cada uno contesta una sola pregunta
            que la persona que busca esto también se está haciendo.
CIERRE      Un párrafo. Cómo lo resuelve PanaClaw, con enlace interno a
            lo que corresponda. Sin llamar «¡contáctanos ya!» — la tarjeta
            de conversión ya la pone la plantilla, debajo, automática.
```

**No hay una llamada a la acción a mitad del post.** Es una decisión de
diseño ya tomada en `src/pages/blog/[slug].astro` — «el post es el gancho
informacional; el cotizador es la conversión»— y el texto no la contradice
metiendo un botón o un «escríbenos» en medio del cuerpo.

### El lead no es un resumen

Es la misma regla del gancho de [`07-redaccion.md`](../../adn/07-redaccion.md) §4,
aplicada a un formato más largo: la primera frase decide si alguien sigue
leyendo o vuelve a Google. Empieza por la escena reconocible o por la pregunta
tal cual se busca, nunca por «en este artículo vamos a ver».

```
✗  En este artículo hablamos sobre cuánto cuesta una página web en Panamá.
✓  Si buscaste esto en Google, ya sabes lo que va a pasar: dos de cada tres
   agencias te van a responder «depende, escríbenos por interno».
```

### Los H2, uno por pregunta

Cada encabezado de sección contesta una pregunta que la persona que llegó
por esa búsqueda también se está haciendo — no un subtema elegido por orden
lógico de exposición. Es la diferencia entre un post que rankea por sus
propios subtítulos y uno que solo rankea por el título.

```
✗  ## Introducción
✗  ## Conclusión
✗  ## Nuestro compromiso con la excelencia
✓  ## ¿Cuánto cuesta el mantenimiento que nadie menciona?
✓  ## ¿A nombre de quién queda el dominio?
```

### El cierre

Un párrafo, con un enlace natural a la página que resuelve lo que el post
acaba de plantear. Se escribe como una frase más, no como un anuncio pegado
al final:

```
✓  Nuestros cuatro planes van de $295 a $1,200, con precio y fecha cerrados
   por escrito antes de empezar. Están publicados aquí, con lo que incluye
   cada uno.
```

El enlace es a una ruta real del sitio — `/planes/`, `/cotizador/`,
`/servicios/#diagnostico`, `/proyectos/`, `/ebot/`, `/seguridad/` — nunca a
una que no exista todavía.

---

## De dónde sale el tema, y de dónde no

**El tema no se inventa ni se elige por lo que suena bien escribir.** Sale de
cruzar dos cosas:

1. **Una pregunta real de alguien que busca.** «Cuánto cuesta», «cómo elegir»,
   «X vs. Y», «por qué me pasó esto» — la forma en la que un dueño de negocio
   panameño escribe en Google, no la forma en la que lo diría un publicista.
2. **Una situación ya catalogada en [`adn/04-audiencia.md`](../../adn/04-audiencia.md)**
   o un pilar de [`adn/01-identidad.md`](../../adn/01-identidad.md). El blog no
   inventa dolores nuevos: usa los seis públicos y las tres cosas contra las
   que se define la marca.

**Y nunca se repite un tema ya publicado.** Antes de proponer uno, se leen los
posts que ya existen en `src/content/blog/` del repositorio del sitio — título,
categoría y `keywords` — y se descarta cualquier ángulo que ya esté cubierto.
El procedimiento completo está en
[`skills/blog-seo/SKILL.md`](../../skills/blog-seo/SKILL.md) paso 1.

---

## Datos, cifras y lo que no se puede afirmar

Un blog de SEO es exactamente el formato donde más tienta rellenar con una
estadística que «suena creíble» — un porcentaje de abandono, una cuota de
mercado, un promedio de precios de la competencia. **Aquí se rompe la regla 4
más que en ningún otro formato, y aquí es donde más caro sale**, porque un
post de blog vive meses y lo lee gente que no tiene ningún otro motivo para
confiar en la marca todavía.

- **Toda cifra de PanaClaw sale de [`datos/precios.json`](../../datos/precios.json)**,
  verificada en el momento de escribirla.
- **La única estadística de sector autorizada** es la de
  [`catalogo/09-prueba.md`](../../catalogo/09-prueba.md): cuatro de cada diez
  personas abandonan una página que tarda más de tres segundos. Se usa **con
  su atribución en la misma frase** — «es un dato del sector, no una medición
  nuestra» — y no se reformula como si fuera un hallazgo propio.
- **Ningún otro número de mercado se inventa**: ni cuota de WordPress, ni
  porcentaje de búsquedas que van a Google, ni rango de precios de «la
  competencia», ni casos anecdóticos sin fuente («cuentas suspendidas el año
  pasado», «marcas con 20,000 seguidores que…»). Si el post necesita ese dato
  para sostenerse, **no se escribe así**: se busca el ángulo que sí se puede
  sostener con lo que hay en [`catalogo/09-prueba.md`](../../catalogo/09-prueba.md),
  o se dice que falta la fuente y se para.
- **Nada sobre cómo se comporta la competencia** — que no publica precios, que
  tarda tres reuniones en dar una cifra. Nadie lo comprobó; está en
  [`operacion/deuda-conocida.md`](../../operacion/deuda-conocida.md) punto 6.

### Lo que hoy no se puede escribir

- **Un post de categoría `casos`** con reto, solución y métricas por
  proyecto: los cuatro proyectos de
  [`catalogo/09-prueba.md`](../../catalogo/09-prueba.md) no tienen esas
  métricas medidas todavía —
  [`operacion/deuda-conocida.md`](../../operacion/deuda-conocida.md) punto 2—.
  Lo que sí se puede escribir con lo que hay: qué es cada proyecto, para quién,
  y su enlace. Sin cifra de resultado.
- **Cualquier comparación con precios reales de agencias panameñas
  nombradas.** Se puede hablar de rangos de mercado en términos generales solo
  si la fuente es verificable y se dice cuál es; si no hay fuente, no se
  publica el rango como si fuera un hecho.

---

## Antes de entregar

- [ ] ¿`title` entre 15 y 90 caracteres?
- [ ] ¿`description` entre 60 y 200 caracteres?
- [ ] ¿`category` es una de las cinco, tal cual está escrita en el enum?
- [ ] ¿`keywords` tiene entre 1 y 6, en minúscula y sin relleno?
- [ ] ¿`readingTime` es un entero entre 2 y 30, razonable para el largo real?
- [ ] ¿El slug no repite uno que ya exista en `src/content/blog/`?
- [ ] ¿El tema no repite el ángulo de un post ya publicado?
- [ ] ¿El lead abre por la escena o la pregunta, no por un resumen ni por la marca?
- [ ] ¿Cada H2 contesta una pregunta real, y no hay «introducción» ni «conclusión»?
- [ ] ¿Alguna llamada a la acción a mitad del cuerpo? → fuera, la pone la plantilla al final
- [ ] ¿Toda cifra de PanaClaw coincide con `datos/precios.json`?
- [ ] ¿Alguna estadística de mercado, de la competencia o un caso anecdótico sin fuente? → fuera
- [ ] Si se usa la cifra del sector (cuatro de cada diez), ¿lleva su atribución en la misma frase?
- [ ] ¿Los enlaces internos van a rutas reales del sitio?
- [ ] ¿Jerga? Búsqueda literal, no de memoria
- [ ] Léelo en voz alta: ¿suena a que alguien le explica algo a otra persona, o a una entrada de blog genérica de agencia?
