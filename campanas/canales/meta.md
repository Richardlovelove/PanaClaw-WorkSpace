# Canal · Meta (Facebook e Instagram)

El canal principal hoy: es el único con medición activa.

> **Las cifras de este archivo no son de PanaClaw.** Son datos de la plataforma y
> del oficio de comprar publicidad, comprobados el **2026-08-19** contra fuentes
> públicas. La tabla de procedencia está al final: **cada una lleva su estado**, y
> dos están marcadas como no verificadas. Ninguna de estas cifras se dice nunca en
> una pieza de cara al cliente — la regla 4 sigue entera; esto es para decidir
> cómo se compra, no para escribirlo en un anuncio.

**Revisado el 2026-08-17** contra el estado real de la plataforma. Meta cambió
dos veces en 2026 —en febrero fusionó el flujo manual con Ventajas+, y en marzo
tocó presupuestos, públicos, creativo y las reglas de contenido generado con
IA— y varias cosas que decía este archivo dejaron de ser ciertas. Lo que cambió
va marcado abajo.

---

## Estado de la medición

- **Píxel de Meta activo:** `1067898639025746`, desde 2026-08-03
- **Eventos:** `PageView` en cada página, y **`Lead` solo en `/gracias/`**
- `/gracias/` es el único punto del sitio donde alguien ha completado algo

---

## Con qué objetivo se arranca

**Cambió.** Este archivo decía «toda campaña de Meta se optimiza contra `Lead`».
Es lo correcto cuando hay volumen, y es una forma de quemar el presupuesto
cuando no lo hay.

### El problema del arranque

Un conjunto de anuncios necesita alrededor de **50 conversiones por semana** del
evento que optimiza para salir de la fase de aprendizaje. `[verificado 2026-08-19]` Por debajo, se queda en
aprendizaje limitado y lo que se lea es ruido.

```
presupuesto mínimo diario = CPA objetivo × 50 ÷ 7
```

Con un lead a 10 dólares eso son unos 71 dólares diarios en un solo conjunto; a
20, unos 143. **Sin histórico de esta marca no se sabe el CPA**, así que
arrancar optimizando `Lead` es apostar el presupuesto a un número que nadie ha
medido.

### Por dónde se arranca

**Conversaciones de WhatsApp.** Tres razones, en orden:

1. El evento es mucho más barato y más frecuente que un `Lead` de formulario, así
   que el conjunto sale de aprendizaje con un presupuesto que esta marca puede
   pagar.
2. **WhatsApp ya es el canal principal de conversación de la marca.** No se está
   inventando un embudo para la campaña: se está pagando por llenar el que ya
   existe.
3. La conversación que abre un anuncio de clic a WhatsApp entra por la **ventana
   gratuita de 72 horas**: lo que se responda ahí dentro no tiene coste de
   mensajería. `[verificado 2026-08-19]`

> **Ojo con la fecha.** Esa ventana de 72 horas de los anuncios sigue en pie,
> pero Meta anunció el 2026-07-01 que **la ventana de servicio gratuita de 24
> horas se acaba el 2026-10-01**: a partir de ahí, responder fuera de la ventana
> del anuncio se cobra por mensaje. Si la campaña arranca cerca de esa fecha,
> compruébalo antes de presupuestar.

Con 20 a 50 dólares diarios se producen datos legibles en cinco a siete días.

| Objetivo | Cuándo |
|---|---|
| **Interacción**, optimizado a conversaciones | El arranque. Máximo volumen, CPM más barato |
| **Clientes potenciales** | Cuando sobren conversaciones y falte calidad |
| **Ventas / `Lead` del píxel** | Cuando haya volumen suficiente para sostener 50 eventos semanales |

**El píxel sigue midiendo mientras tanto.** No se apaga: se está acumulando el
histórico que hace falta para poder pasar a optimizar contra `Lead` más adelante.

---

## Estructura de campaña

**Cambió.** Este archivo pedía «al menos 4 variantes». Hoy eso no es una prueba.

La prueba interna de Meta que sostiene la recomendación actual: **un conjunto con
25 creativos diversos produjo un 17 % más de conversiones a un 16 % menos de
coste** que cinco conjuntos de cinco creativos cada uno. `[verificado 2026-08-19]`

Sale del cambio de motor de entrega de Meta —el que la industria llama
**Andromeda**— y es lo que explica por qué la estructura ganadora hoy es la
contraria a la de hace dos años.

```
1 campaña  →  1 conjunto  →  de 8 a 12 conceptos distintos dentro
```

Menos campañas, menos conjuntos, más creativos y público amplio. Repartir el
mismo presupuesto entre cinco conjuntos es repartir también la señal, y ninguno
llega a aprender.

**La regla de «una hipótesis por variante» no cambia.** Es lo que separa doce
anuncios de uno repetido doce veces. Las cuatro hipótesis están en
[`prompts/texto/anuncios.md`](../../prompts/texto/anuncios.md): velocidad,
propiedad, plazo y precio publicado.

---

## La diversidad creativa contra el sistema visual

Es el choque que hay que entender antes de producir, porque no es obvio y cuesta
alcance.

El motor de entrega **agrupa los creativos que se parecen bajo una misma
identidad interna y los hace competir entre sí en vez de ampliar el alcance.** El
colapso empieza a documentarse por encima del 60 % de parecido; la recomendación
de oficio es quedarse **por debajo del 40 %** y renovar cada dos o tres semanas.
`[verificado 2026-08-19]`

Y el sistema visual de PanaClaw es deliberadamente idéntico entre piezas: mismo
bloque de estilo, misma familia de escena, mismo velo, un solo acento. **Esa
igualdad es lo que hace reconocible la marca, y es exactamente lo que el
algoritmo colapsa.**

**No se rompe el sistema.** La diversidad que cuenta es de concepto y de formato:

| Eje que SÍ se varía | De dónde sale |
|---|---|
| El dolor del que se parte | Las seis situaciones de [`adn/04-audiencia.md`](../../adn/04-audiencia.md) |
| El ángulo | Los cuatro de [`prompts/texto/anuncios.md`](../../prompts/texto/anuncios.md) |
| La escena madre | Las siete de [`prompts/README.md`](../../prompts/README.md) |
| El formato | Vertical, vertical de vídeo, cuadrado, carrusel |

| Eje que NO se varía |
|---|
| El bloque de estilo, que se copia literal |
| La paleta y el acento único |
| Las dos familias tipográficas |

Con cuatro ángulos y siete escenas ya salen los ocho a doce conceptos sin
inventar nada.

---

## Formatos

| Ubicación | Proporción | Píxeles |
|---|---|---|
| Feed | 4:5 | 1080 × 1350 |
| Feed cuadrado | 1:1 | 1080 × 1080 |
| Stories y Reels | 9:16 | 1080 × 1920 |

**Vídeo e imagen, no una cosa u otra.** El vídeo vertical de aspecto nativo
compra atención más barata: **la ubicación de Reels sale alrededor de un 26 % más
barata por clic** que el feed de Facebook. `[verificado 2026-08-19]`

> **No verificado:** que el estático produzca «entre el 60 y el 70 % de las
> conversiones». La cifra circula por el oficio y no se le encuentra fuente
> primaria; y lo que sí está documentado apunta en la otra dirección —el feed
> convierte de forma más constante que Reels, pero nadie publica ese reparto.
> **Trátalo como intuición, no como dato.**

> **No verificado:** el reparto **70 % vídeo / 30 % imagen**. No es una
> recomendación de Meta; es una de varias que circulan, y las fuentes consultadas
> dan repartos distintos entre sí. **No lo defiendas como si fuera un estándar.**

Lo que sí se sostiene: **una cuenta de un solo formato queda por debajo de una
que mezcla**, porque el motor necesita creativos que no se parezcan entre sí (la
sección de arriba). El reparto exacto lo decide la primera campaña de esta marca,
midiéndolo — no una cifra copiada.

> **Hueco conocido:** hay estructura de guion en
> [`prompts/video/video-corto.md`](../../prompts/video/video-corto.md), pero no
> hay una cadena de producción de vídeo equivalente a la de imagen. Mientras no
> la haya, dilo al entregar en vez de fingir que el reparto 70/30 es posible.

---

## Los primeros 125 caracteres

Es el anuncio entero. Después viene el «ver más», y **lo pulsa alrededor del 1 %**.
`[verificado 2026-08-19]`

**Ahí tienen que estar el gancho y la cifra.** El giro y el límite pueden caer
después.

```
Tu web tarda y la gente se va antes de ver lo que vendes. $295, lista en 72 h.
```

78 caracteres, y ya está todo lo esencial.

---

## Públicos

**Cambió.** La segmentación fina por intereses quedó retirada: hoy se arranca en
amplio y es la plataforma la que lee el creativo para decidir a quién enseñárselo.

### Frío

- **Ubicación:** Panamá
- **Edad:** 25–55
- **Intereses: ninguno.** No es pereza — es lo que la plataforma pide ahora. Lo
  que antes hacía la segmentación lo hace hoy el creativo
- **Tope de cliente existente: entre el 10 % y el 20 %**, para que el presupuesto
  se vaya a gente nueva y no a quien ya conoce la marca

> Lo que sí sigue siendo cierto: **nunca segmentes por «diseño web» ni
> «tecnología»**. Eso alcanza a colegas del sector, no a clientes. Si algún día
> vuelve a haber segmentación fina, esa sigue siendo la trampa.

### Tibio — remarketing de sitio

Requiere el píxel, que ya está.

| Público | Qué anuncia |
|---|---|
| Visitó `/planes/` sin llegar a `/gracias/` | La objeción del precio, o el cotizador |
| Visitó `/ebot/` | Los dos costos de terceros, publicados |
| Visitó `/seguridad/` | El procedimiento de los cuatro pasos |
| Visitó `/cotizador/` sin enviar | Una promesa: el código queda a tu nombre |

### Parecidos (lookalike)

**Todavía no.** Hacen falta suficientes eventos para que el público parecido
signifique algo. Sin campañas corridas, un parecido hoy se construye sobre ruido.

---

## Contenido generado con IA: hay que declararlo

**Nuevo, y es el que puede tumbar los anuncios el primer día.**

Desde marzo de 2026 Meta **exige declarar el contenido generado o modificado con
inteligencia artificial**, y no declararlo se ha vuelto uno de los motivos de
rechazo más frecuentes.

**Todos los fondos de esta marca salen de un generador de imagen.** Va declarado
en cada anuncio, desde el primero.

No es solo cumplimiento: encaja con el argumento de la marca mejor que con el de
nadie. La agencia que publica lo que no incluye no tiene ningún problema en
publicar cómo hace sus fondos.

---

## Ventajas+: qué se acepta y qué se desactiva

**Cambió.** Este archivo tenía «Ventajas+ con creativo automático» en la lista de
lo que hay que rechazar entero. En febrero de 2026 Meta fusionó el flujo manual
con el de Ventajas+ en uno solo, con la automatización activada por defecto en
público, ubicaciones y presupuesto, y cada una desactivable por separado.

Rechazarlo todo hoy es pelearse con el flujo por defecto. La distinción correcta:

| Automatización | Qué se hace | Por qué |
|---|---|---|
| Público automático | **Aceptar** | Es como se entrega ahora. La segmentación fina ya no existe |
| Ubicaciones automáticas | **Aceptar** | Reels es donde está el coste por clic bajo |
| Presupuesto automático | **Aceptar** | Reparte mejor que a mano con pocos datos |
| **Mejoras automáticas de creativo** | **Desactivar** | Reencuadran, aplican filtros y cambian el color. Con un sistema de negro y un único acento, cualquier ajuste automático lo rompe |

**Lo demás que Meta sigue empujando y sigue habiendo que rechazar:**

| Meta sugiere | Por qué no |
|---|---|
| Añadir emojis al texto | Prohibido en la marca, también en pauta |
| «Mejorar» el copy con su IA | Mete exclamaciones y relleno de agencia |
| Recortar la imagen a otras proporciones | Parte el sujeto y tapa el carril del titular |
| Añadir un botón de «Reservar ahora» | La llamada a la acción se elige a propósito |

---

## Presupuesto y lectura

No hay histórico de esta marca, así que **cualquier cifra de rendimiento propia
sería inventada**. Lo que sí se puede decir:

- **No hay CPM ni coste por clic publicado para Panamá.** Lo único sólido es la
  dirección: **Latinoamérica está entre las regiones más baratas.** Los tramos que
  se citan para esos mercados van de 0,50 a 4 dólares de CPM según la fuente, y la
  media global que publica cada informe es distinta —se encontraron 6,59 y 11,76
  el 2026-08-19—. **Sirve para saber que el terreno es barato; no sirve para
  presupuestar**, y ninguna de esas cifras se cita como si fuera la buena.
  `[la media global de 7,47 que decía este archivo no se pudo confirmar y se retiró]`
  La cifra de Panamá se mide la primera semana.
- **Las subidas de presupuesto van del 20 % cada tres o cuatro días.** Un salto
  mayor devuelve el conjunto a la fase de aprendizaje. `[verificado 2026-08-19]`
- **No se lee nada antes de tener eventos suficientes.** Un ganador declarado con
  tres conversiones es ruido.
- **Renovar creativos cada dos o tres semanas**, no cuando bajen los resultados:
  para entonces ya se pagó el desgaste.

---

## Antes de subir

- [ ] ¿El objetivo es conversaciones, y no `Lead` del sitio, mientras no haya
      volumen para sostener 50 eventos semanales?
- [ ] ¿Una campaña, un conjunto, de 8 a 12 conceptos distintos dentro?
- [ ] ¿Cada concepto varía dolor, ángulo, escena o formato — y ninguno varía el
      bloque de estilo?
- [ ] ¿Está declarado el contenido generado con IA en cada anuncio?
- [ ] ¿Están desactivadas las mejoras automáticas de creativo, y aceptadas las de
      público, ubicaciones y presupuesto?
- [ ] ¿Tope de cliente existente entre el 10 % y el 20 %?
- [ ] ¿Gancho y cifra dentro de los primeros 125 caracteres?
- [ ] ¿4:5 para feed, 9:16 para Reels y stories?
- [ ] ¿El texto de la story queda fuera de las zonas seguras?
- [ ] ¿La cifra coincide con [`datos/precios.json`](../../datos/precios.json)?
- [ ] ¿La llamada a la acción de WhatsApp va sin número?
- [ ] ¿Se está prometiendo algún resultado que no se pueda comprobar el primer día?
- [ ] ¿Alguna cifra de esta página se coló en el texto de un anuncio? → ninguna
      sale de aquí; las que se dicen en una pieza salen de `datos/precios.json`

---

## Procedencia de las cifras de esta página

Comprobado el **2026-08-19** contra fuentes públicas del sector. Se anota aquí
por la misma razón que se anota todo lo demás: **una cifra sin fecha deja de ser
cierta sin que nadie la toque.**

| Cifra | Estado |
|---|---|
| 50 conversiones semanales para salir de aprendizaje | **Verificado.** Es el umbral que documenta la propia Meta |
| 25 creativos en un conjunto: +17 % conversiones, −16 % coste | **Verificado.** Prueba interna de Meta, ligada a su motor de entrega actual |
| Parecido por debajo del 40 %, renovar cada 2–3 semanas | **Verificado.** El colapso se documenta por encima del 60 %; 40 % es el margen de oficio |
| De 8 a 12 conceptos distintos | **Verificado** para presupuestos pequeños, que es el caso |
| Reels ~26 % más barato por clic que el feed | **Verificado.** Es Reels de Instagram contra feed de Facebook |
| Los primeros 125 caracteres, y ~1 % pulsa «ver más» | **Verificado** |
| Subidas de presupuesto del 20 % cada 3–4 días | **Verificado** |
| Ventana gratuita de 72 h del clic a WhatsApp | **Verificado**, con la fecha del 2026-10-01 encima. Ver arriba |
| Meta fusionó el flujo manual con Ventajas+ (feb 2026) | **Verificado** |
| Declarar contenido generado con IA (mar 2026) | **Verificado**, y es de los motivos de rechazo más frecuentes |
| El estático produce el 60–70 % de las conversiones | **NO VERIFICADO.** Circula sin fuente primaria y lo documentado apunta en otra dirección |
| Reparto 70 % vídeo / 30 % imagen | **NO VERIFICADO.** No es recomendación de Meta y las fuentes se contradicen |
| Media global de CPM de 7,47 | **RETIRADO.** No se pudo confirmar: los informes consultados dan 6,59 y 11,76 |

**Qué hacer con las dos no verificadas y la retirada.** No se borran del oficio —
siguen siendo la intuición con la que trabaja medio sector— pero **no se
defienden como dato, no se le pasan al cliente y no se usan para justificar un
presupuesto.** Cuando esta marca corra su primera campaña, sus propios números
sustituyen a los tres y llevan su fecha, como todo lo demás.

> **Y una que no se comprobó porque no es de este archivo:** las zonas seguras de
> story que declara
> [`campanas/plantillas/estructura-anuncio.md`](../plantillas/estructura-anuncio.md)
> —15 % arriba y 20 % abajo— no coinciden con la especificación unificada de
> Stories y Reels de marzo de 2026. Está señalado para que lo decida quien lleva
> el diseño; ver la nota de esa página.
