# Entregable · Campaña Meta de arranque · 2026-08

> **Esto no es doctrina del repositorio.** Es un entregable con fecha, producido
> contra el ADN el 2026-08-19. Cuando la campaña termine, este archivo **se
> borra** — la regla de este repositorio es que no se guardan copys finales
> (`CLAUDE.md` §7). Lo que sí se queda, si algo de aquí se aprueba como norma,
> sube a `datos/`, `campanas/` o `prompts/` por la vía de
> `operacion/sincronizacion.md`.

Presupuesto: **$15 al día**. Marca sin clientes, sin seguidores y sin histórico
de pauta.

---

## PARTE 0 · Lo que hay que resolver ANTES de gastar un dólar

Va primero porque tres de estos puntos impiden que la campaña exista, no que
rinda peor. Salen de `operacion/deuda-conocida.md`.

| # | Qué falta | Efecto | Quién lo desbloquea |
|---|---|---|---|
| 1 | **Página de Facebook, cuenta de Instagram y WhatsApp Business conectados** | Sin página no hay anuncio. Sin WhatsApp Business conectado no hay anuncio de mensajes, que es el objetivo entero de esta campaña | Dueño de la marca |
| 2 | **Declaración de contenido generado con IA activada en cada anuncio** | Desde marzo de 2026 Meta lo exige. No declararlo es de los motivos de rechazo más frecuentes, y todos los fondos de esta marca los genera un motor de imagen | Quien sube los anuncios |
| 3 | **Mejoras automáticas de creativo desactivadas** | Reencuadran, filtran y cambian el color. Con un fondo `#100101` y un solo acento `#FF5100`, cualquier ajuste automático rompe la pieza | Quien sube los anuncios |
| 4 | Dominio propio | Los 12 anuncios van a WhatsApp, así que **hoy no bloquea**. El día que se anuncie el sitio, sí: un anuncio que cae en un subdominio prestado contradice «el sitio es tuyo» en el primer clic | Dueño de la marca |

El punto 4 es, además, la razón técnica por la que el destino de las doce piezas
es WhatsApp y no la web.

---

## PARTE 1 · La estructura de campaña

Esta parte se aprueba **antes** de producir los creativos
(`campanas/README.md`, pasos 1–4 antes del 5). Si cambia, cambian las piezas.

```
1 CAMPAÑA  →  1 CONJUNTO  →  12 CREATIVOS
```

Un solo conjunto, con todo el presupuesto dentro. Repartir $15 entre dos
conjuntos es repartir también la señal y que ninguno aprenda.

### Objetivo

**Interacción, optimizado a conversaciones de WhatsApp.** No `Lead` del píxel.

El motivo, con los números de `campanas/canales/meta.md`: un conjunto necesita
unas 50 conversiones semanales del evento que optimiza para salir de la fase de
aprendizaje. Con $15 al día son $105 a la semana; **50 conversaciones a la <!-- v: $105 es 15 × 7, aritmética de presupuesto de pauta, no un precio del catálogo -->
semana solo salen si una conversación cuesta $2.10 o menos.** Un `Lead` de <!-- v: $2.10 es 105 ÷ 50, el techo de coste por conversación, no un precio del catálogo -->
formulario no cuesta eso en ningún mercado, y una conversación de WhatsApp en
Panamá podría — es lo que la primera semana va a medir.

**El píxel `1067898639025746` se queda encendido.** No se apaga: está acumulando
el histórico que hace falta para poder pasar a optimizar contra `Lead` más
adelante.

### Público

| Campo | Valor |
|---|---|
| Ubicación | Panamá |
| Edad | 25–55 |
| Intereses | **Ninguno** |
| Tope de cliente existente | 10 %–20 % |
| Públicos parecidos | No. Todavía no hay eventos suficientes; un parecido hoy se construye sobre ruido |

Intereses en cero no es pereza: es como entrega Meta hoy. Lo que antes hacía la
segmentación lo hace ahora el creativo, y por eso hay doce y no uno.

**La trampa que sigue en pie:** nunca segmentar por «diseño web» ni
«tecnología». Eso alcanza a colegas del gremio, no a clientes.

### Automatizaciones

| Automatización | Qué se hace |
|---|---|
| Público automático | Aceptar |
| Ubicaciones automáticas | Aceptar |
| Presupuesto automático | Aceptar |
| **Mejoras automáticas de creativo** | **Desactivar** |
| Emojis sugeridos por Meta | Rechazar |
| «Mejorar» el copy con la IA de Meta | Rechazar |
| Recortar la imagen a otras proporciones | Rechazar |
| Botón de «Reservar ahora» | Rechazar |

### Destino

**WhatsApp, en los doce.** Una sola llamada a la acción por pieza: una pieza con
dos no tiene dos, tiene cero.

- Botón: **Enviar mensaje**
- El número **no se imprime** en ninguna pieza ni en ningún texto
- Enlace, si hace falta componerlo a mano:
  `https://wa.me/19406046565?text={mensaje-codificado-en-url}`
- Mensaje precargado, por producto:
  - Conceptos de Start → `Hola PanaClaw, me interesa el plan Start`
  - Conceptos de Diagnóstico → `Hola PanaClaw, quiero el Diagnóstico de Ventas`

### Los dos productos de entrada

Solo dos cifras del catálogo son lo bastante bajas para decidirse dentro de un
anuncio en frío:

| Producto | Precio | Plazo | Conceptos |
|---|---|---|---|
| PanaClaw Start | $295 | 72 h | 01, 02, 03, 04, 05, 08 |
| Diagnóstico de Ventas | $49 | Informe + llamada de 30 min en 48 h | 06, 07, 09, 10, 11, 12 |

Launch $450, Corporate $850, Commerce $1,200, eBot $499 y los planes de
seguridad **no se anuncian en frío**. Se venden dentro de la conversación de
WhatsApp, que es donde está el margen y donde se califica.

### Presupuesto y lectura

- **$15 al día**, todo en un conjunto.
- El repositorio documenta que con $20–50 diarios salen datos legibles en 5–7 <!-- v: rango de presupuesto diario de campanas/canales/meta.md, no un precio del catálogo -->
  días. Eso son $100–$140 de gasto. **A $15 al día ese mismo gasto tarda de 7 a <!-- v: gasto acumulado calculado sobre el rango anterior, no un precio del catálogo -->
  10 días** — es aritmética sobre el rango publicado, no una predicción de
  rendimiento.
- **No se lee nada antes de eso.** Un ganador declarado con tres conversaciones
  es ruido.
- Las subidas de presupuesto van del **20 % cada tres o cuatro días**. Un salto
  mayor devuelve el conjunto a aprendizaje.
- **No hay CPM ni coste por clic de Panamá publicado.** La cifra se mide la
  primera semana. Cualquier número propio antes de eso sería inventado.
- **Renovar creativos cada dos o tres semanas**, no cuando bajen los resultados:
  para entonces ya se pagó el desgaste.

### Qué se mide, y qué no

Se mide: conversaciones iniciadas, coste por conversación, y `Lead` en
`/gracias/` acumulándose de fondo.

**No se mide, y no se propone:** coste por cliente, tasa de conversión por
canal, retorno de la inversión. Con un píxel y un evento, esas métricas no
existen.

### Los 12 creativos, en una vista

| # | Público | Producto | Ángulo (hipótesis) | Altura del titular | Formato | Escena madre |
|---|---|---|---|---|---|---|
| 01 | No tiene sitio | Start $295 | Precio publicado | Consecuencia | 4:5 | 7 · Esfera de roca |
| 02 | No tiene sitio | Start $295 | Plazo | Consecuencia | 4:5 | 3 · Hélice de cristal |
| 03 | No tiene sitio | Start $295 | Velocidad | Consecuencia | 9:16 | 1 · Proyectil |
| 04 | No tiene sitio | Start $295 | Propiedad | Consecuencia | 4:5 | 4 · Servidores |
| 05 | No tiene sitio | Start $295 | Precio publicado · el límite como diferenciador | Condición | 9:16 | 7 · Esfera de roca |
| 06 | WordPress que da vergüenza | Diagnóstico $49 | Velocidad | Consecuencia | 4:5 | 1 · Proyectil |
| 07 | WordPress que da vergüenza | Diagnóstico $49 | Precio publicado | Hecho | 4:5 | 6 · Cintas de luz |
| 08 | No tiene sitio | Start $295 | Propiedad | Consecuencia | 9:16 | 4 · Servidores |
| 09 | WordPress que da vergüenza | Diagnóstico $49 | Plazo | Hecho | 4:5 | 3 · Hélice de cristal |
| 10 | Invierte en publicidad | Diagnóstico $49 | Velocidad | Consecuencia | 4:5 | 1 · Proyectil |
| 11 | Invierte en publicidad | Diagnóstico $49 | Precio publicado | Consecuencia | 9:16 | 6 · Cintas de luz |
| 12 | Invierte en publicidad | Diagnóstico $49 | Plazo | Hecho | 4:5 | 1 · Proyectil |

**Reparto de ángulos:** precio publicado 4 · plazo 3 · velocidad 3 · propiedad 2.
**Alturas:** 8 consecuencia · 3 hecho · 1 condición. Una sola pieza abre por el
límite, muy por debajo del tope de una de cada tres.

**Lo que varía entre conceptos:** dolor, ángulo, escena madre y formato.
**Lo que no varía nunca:** el bloque de estilo, la paleta, el acento único y las
dos familias tipográficas. El motor de entrega agrupa creativos que se parecen y
los hace competir entre sí; la diversidad que cuenta es de concepto, no de
estilo.

---

## PARTE 2 · El prompt maestro

Se pega entero en Meta AI. Devuelve un documento HTML con los 12 creativos
compuestos, descargables en PNG a tamaño real, y debajo de cada uno su copy de
anuncio en texto seleccionable.

````
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. QUÉ ERES Y QUÉ NO HACES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Vas a hacer dos cosas y ninguna más: generar 12 fondos de imagen y montar un
documento HTML donde esos fondos se ven ya compuestos con su texto y se pueden
descargar.

No escribas, no redactes, no completes, no acortes, no traduzcas y no
"mejores" ningún texto. Todo el texto de este documento ya está escrito más
abajo. Cópialo carácter por carácter, con sus tildes, sus eñes y sus puntos
finales. Si algo te parece incompleto, déjalo como está: está así a propósito.
No añadas ninguna cifra, porcentaje, estadística, plazo, testimonio ni
beneficio que no esté escrito literalmente en este documento.

Tampoco añadas emojis, signos de exclamación, ni palabras en mayúscula de
énfasis. No hay ninguno en lo que te doy y no debe haber ninguno en lo que
devuelvas.

Los fondos que generes no llevan ni una sola letra, cifra, icono ni logotipo
dentro. El texto se compone encima, en el HTML, con fuentes reales.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
2. EL SISTEMA VISUAL
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

COLOR — cinco valores, ninguno más
  #100101  fondo maestro de todo. Negro cálido, no negro puro
  #FF5100  acento ÚNICO: símbolo, antetítulo, un tramo del titular
  #FF1E1E  SOLO fondos e imagen. Prohibido en cualquier letra
  #FFF7F7  texto principal, titular, cifra, wordmark
  #BABABA  bajada, nota, numerador

  Prohibido: azul de cualquier tono, cian, verde, morado, amarillo, rosa,
  pastel, #FFFFFF puro, #000000 puro, degradados multicolor, y cualquier
  segundo color de acento junto al naranja.

TIPOGRAFÍA — dos familias con los roles cerrados
  Antonio 700   titular y cifra. Nunca baja a texto pequeño
  Archivo       antetítulo (500), bajada (300), nota (400), wordmark (700)

  Prohibida cualquier otra familia, sin excepción, incluidas las que un editor
  sugiere por defecto para este aspecto. Si Antonio o Archivo no cargan, para
  y dilo: no sustituyas por la más parecida.

RETÍCULA — lienzo 1080×1350 (formato 4:5, ocho piezas)
  Margen lateral        72 izquierda, 1008 derecha. Ancho útil 936
  Todo alineado a la izquierda en x=72. El símbolo es la única excepción
  Símbolo               88 de ancho × 72 de alto, centrado horizontalmente,
                        caja de y=96 a y=168. EMPIEZA en 96, no está centrado
                        en 96. NO es cuadrado: proporción 100 × 81.56
  Bloque de texto       anclado por su centro óptico en y=594
  Wordmark              x=72, base del bloque en y=1254

RETÍCULA — lienzo 1080×1920 (formato 9:16, cuatro piezas)
  Margen lateral        idéntico: 72 y 1008. Ancho útil 936
  Zonas seguras         nada de texto ni símbolo por encima de y=288 ni por
                        debajo de y=1536. Ahí caen la interfaz y los botones
  Símbolo               88 × 72, centrado, caja de y=312 a y=384
  Bloque de texto       anclado por su centro óptico en y=880
  Wordmark              x=72, base del bloque en y=1500

ESCALA — píxeles idénticos en los dos lienzos, porque los dos miden 1080 de ancho
  Titular XL   Antonio 700, 132 px, interlínea 0.88, tracking -0.01em, #FFF7F7
  Titular L    Antonio 700, 112 px, interlínea 0.88, tracking -0.01em, #FFF7F7
  Antetítulo   Archivo 500, 24 px, tracking 0.16em, VERSALITAS, #FF5100,
               margen inferior 28
  Bajada       Archivo 300, 30 px, interlínea 1.45, #BABABA, margen superior 36
  Cifra        Antonio 700, 76 px, tracking 0, VERSALITAS, #FFF7F7,
               margen superior 44
  Nota         Archivo 400, 20 px, interlínea 1.5, tracking 0.14em,
               VERSALITAS, #BABABA, margen superior 28
  Wordmark     Archivo 700, 30 px, tracking 0.22em, VERSALITAS, #FFF7F7,
               con un punto final "." en #FF5100

  Titular y cifra siempre en versalitas. La bajada nunca. Cada pieza de abajo
  lleva escrito su tamaño de titular: úsalo, no lo recalcules.

EL ORDEN DEL BLOQUE DE TEXTO — no se negocia
  ANTETÍTULO
  TITULAR
  CIFRA
  NOTA

  La cifra va SIEMPRE después del titular, nunca antes. Si lo primero que se
  lee en la pieza es un número, está al revés. Ninguna de estas 12 piezas
  lleva bajada.

EL ACENTO NARANJA
  Un solo tramo del titular va en #FF5100. Uno, continuo, y nunca más de la
  mitad de los caracteres. Todo lo demás del titular en #FFF7F7.
  Cada pieza de abajo trae marcado su tramo naranja entre >>> y <<<.
  Esas marcas NO se imprimen: indican qué va en naranja.
  #FF1E1E no toca ni una letra.

LOS CORTES DE LÍNEA
  Los cortes del titular están escritos, uno por línea. Respétalos
  exactamente. No los recalcules, no los justifiques, no los reflowees.

EL VELO
  La imagen va a sangre, cubriendo el lienzo entero.
  Brillo de la imagen: 0.65
  Encima, un degradado lineal desde el borde donde cae el texto hacia el
  opuesto: de rgba(16,1,1,0.92) a rgba(16,1,1,0.10)
  Ninguna caja, tarjeta, franja, rectángulo semitransparente ni sombra detrás
  del texto. El contraste lo pone el velo, que es continuo y no tiene borde.

EL SÍMBOLO
  Es una garra de tres zarpazos atravesando un par de corchetes angulares.
  Dibújalo como SVG en línea, en #FF5100 plano, sin degradado y sin efectos,
  con viewBox="0 0 100 81.56" y fill-rule="evenodd".

  M73.43 28.64L54.69 50.19L42.73 77.94L67.38 50.63L67.45 47.83L68.19 44.36Z M81.03 21.85L73.95 28.93L85.68 40.52L67.9 58.38L75.2 65.76L100 40.52Z M74.61 15.5L74.39 15.5L73.8 16.09L73.65 16.39L73.28 16.61L72.69 17.2L72.62 17.42L67.6 22.44L67.6 22.59L72.1 27.01L72.25 27.01L79.19 20.08Z M25.17 15.35L0 40.3L25.39 65.32L32.32 58.16L14.32 40.37L32.18 22.36Z M59.26 1.77L32.69 28.79L32.62 31.52L31.59 36.31L26.64 51.74L45.68 29.75L50.41 19.41Z M75.94 0.15L52.18 27.24L50.85 31L41.62 43.62L23.91 81.56L48.12 52.55L49.89 47.98L59.04 35.65Z

  Sin fill-rule="evenodd" los huecos de los corchetes se rellenan y el logo
  sale como una mancha. Sin la proporción 100 × 81.56 el símbolo se deforma.

EL WORDMARK
  El texto es exactamente: PANACLAW.
  PANACLAW en #FFF7F7 y el punto final en #FF5100. Es un solo punto y va en
  naranja. No lo partas en dos colores, no lo escribas sin el punto.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
3. EL CONTRATO DEL HTML
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Devuelve UN documento HTML completo, con las 12 imágenes dentro del propio
archivo, que se abra en el navegador sin depender de nada externo.

FUENTES — sin esto todo lo demás da igual
  Carga Antonio y Archivo desde Google Fonts:
  https://fonts.googleapis.com/css2?family=Antonio:wght@700&family=Archivo:wght@300;400;500;700&display=swap
  Espera a document.fonts.ready antes de dibujar cualquier canvas.

CADA PIEZA, A MEDIDA REAL
  Las ocho piezas 4:5 se dibujan a 1080×1350 exactos.
  Las cuatro piezas 9:16 se dibujan a 1080×1920 exactos.
  En pantalla se pueden ver reducidas con transform: scale(), pero el lienzo
  que se exporta mide exactamente eso.

BOTONES DE DESCARGA
  Cada pieza lleva su botón que la baja en PNG a tamaño real, dibujando la
  imagen y el texto sobre un <canvas> del tamaño que le toca. Sin librerías
  externas. Y un botón que las descargue todas.

LAS CINCO TRAMPAS DEL EXPORTADOR
  Aquí es donde falla, y falla en silencio: la vista previa se ve perfecta y
  el PNG sale roto.

  1. ctx.letterSpacing NO se reinicia al cambiar ctx.font. Si lo usas para el
     tracking del wordmark, ponlo a '0px' inmediatamente después de dibujarlo.
     Si no, el tracking se filtra a la cifra, al antetítulo y al titular, y el
     titular se sale del lienzo.

  2. Fija ctx.textBaseline='top' antes de dibujar y usa la misma Y que el
     maquetado. Con el valor por defecto ('alphabetic') el texto del PNG cae
     más abajo que en la vista previa.

  3. Mide el alto real del bloque de texto con getBoundingClientRect() del
     elemento ya maquetado. No lo estimes multiplicando líneas por interlínea:
     el anclaje al centro óptico se descuadra respecto a lo que se ve.

  4. El símbolo EMPIEZA en y=96 en las piezas 4:5 y en y=312 en las 9:16; no
     está centrado en esos valores. Su caja mide 88 de ancho por 72 de alto.
     No es cuadrado.

  5. Un botón que lanza 12 descargas seguidas lo bloquea el navegador a la
     tercera. O agrupas en un ZIP de verdad, o el botón se llama "descargar
     una por una" y avisa de que hay que permitirlo.

DEBAJO DE CADA PIEZA
  En texto seleccionable, para copiar y pegar en el editor de anuncios, y
  copiado literal de lo que te doy más abajo:
    - Texto principal
    - Titular del anuncio
    - Descripción
    - Botón
    - Mensaje precargado de WhatsApp
    - El prompt del fondo, por si hay que regenerar esa imagen

LA INTERFAZ DEL DOCUMENTO
  Fondo #100101, texto #FFF7F7, acento #FF5100. Es una herramienta interna,
  pero se mira todo el mes.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
4. EL BLOQUE DE ESTILO — idéntico en las 12, palabra por palabra
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Estilo: fotografía cinematográfica de materia oscura incandescente. Fondo
negro cálido #100101, casi sin iluminación ambiente. La única luz nace del
propio sujeto: brasas y filamentos incandescentes en naranja #FF5100 y rojo
#FF1E1E. Materiales: obsidiana pulida, cristal negro, roca fundida, metal
oscuro con vetas encendidas. Contraste altísimo, negros profundos que se
tragan los bordes del encuadre, reflejos especulares muy contenidos.
Atmósfera de estudio, aire limpio, sin niebla lechosa. Grano fino de película.
Sin personas.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
5. LOS NEGATIVOS — idénticos en las 12, palabra por palabra
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

No incluyas: personas, oficinas, laptops ni pantallas; ningún azul, verde,
morado ni tono pastel; nada de blanco puro ni fondos claros; nada de luz
natural ni exteriores; ningún texto, letra, número, icono, logotipo ni
gráfico; nada de estética de stock corporativo; nada de candados, escudos,
bombillas, engranajes ni gráficos de barras.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
6. LOS DOS ENCUADRES — se pegan al final del prompt de cada fondo
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ENCUADRE 4:5 (piezas 01, 02, 04, 06, 07, 09, 10, 12)
Encuadre: composición vertical 4:5. Los 180 píxeles superiores y los 160
inferiores del cuadro quedan en negro limpio, sin ninguna forma, resplandor
ni reflejo, ni siquiera difuso. El sujeto vive entre esas dos bandas y se
abre hacia los bordes laterales y hacia el tercio superior. La banda central
del cuadro queda en negro limpio, con la incandescencia muriendo antes de
entrar en ella.

ENCUADRE 9:16 (piezas 03, 05, 08, 11)
Encuadre: composición vertical 9:16. Los 420 píxeles superiores y los 480
inferiores del cuadro quedan en negro limpio, sin ninguna forma, resplandor
ni reflejo, ni siquiera difuso. El sujeto vive entre esas dos bandas y se
abre hacia los bordes laterales. La banda central del cuadro, entre 590 y
1170 píxeles de altura, queda en negro limpio, con la incandescencia
apagándose antes de llegar a ella.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
7. LAS 12 PIEZAS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

──────────────── PIEZA 01 · 1080×1350 ────────────────
FONDO
Una esfera de roca incandescente flotando sola en el centro de una cámara de
piedra negra. Es pequeña respecto al espacio: la cámara se pierde en la
oscuridad a su alrededor y solo se adivinan los muros más cercanos por el
resplandor que reciben. [BLOQUE DE ESTILO] [ENCUADRE 4:5] [NEGATIVOS]

ANTETÍTULO   PANACLAW START
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=594
             SABES LO QUE
             CUESTA >>>ANTES
             DE ESCRIBIRME.<<<
CIFRA        $295
NOTA         72 HORAS. EL RELOJ EMPIEZA CUANDO ME DAS TU MATERIAL Y LA MITAD
             DEL PAGO.

TEXTO PRINCIPAL
Preguntas cuánto cuesta una página y te dan un rango. $295, lista en 72 horas.
Pasa porque la cotización es la venta: primero la reunión, después el número.
Aquí el número está escrito antes de que me escribas, y al lado está la lista
de lo que no entra.
El reloj empieza cuando me das tus textos y la mitad del pago. Escribirlos yo
es otro trabajo y se cotiza; ordenarlos contigo va incluido en la conversación.
Escríbeme por WhatsApp y te digo cuál te encaja, o que no te hace falta ninguno.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   $295. Lista en 72 horas.
DESCRIPCIÓN           El precio y lo que no incluye, publicados.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, me interesa el plan Start

──────────────── PIEZA 02 · 1080×1350 ────────────────
FONDO
Una hélice de bloques de cristal rojo encajados uno tras otro, ascendiendo en
espiral. Cada bloque entra en el anterior con un ajuste exacto y el punto de
encaje brilla más que el resto de la pieza. [BLOQUE DE ESTILO] [ENCUADRE 4:5]
[NEGATIVOS]

ANTETÍTULO   PANACLAW START
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=594
             TU PÁGINA ABIERTA
             >>>EN TRES DÍAS,<<<
             NO EN TRES MESES.
CIFRA        $295
NOTA         72 HORAS DESDE QUE ME DAS TUS TEXTOS Y LA MITAD DEL PAGO. TE
             AYUDO A ORDENARLOS MIENTRAS HABLAMOS.

TEXTO PRINCIPAL
Preguntaste por una web y te dijeron un mes y medio. Van tres. $295 y 72 horas.
Pasa porque cada proyecto se empieza desde cero. El mío no: lo que se repite ya
está resuelto, así que el tiempo se va en lo tuyo.
Las 72 horas cuentan desde que me das tu material y la mitad del pago. Esperar
los textos es la causa número uno de retraso, así que te ayudo a ordenarlos
mientras hablamos.
Escríbeme por WhatsApp y te digo cuál te encaja, o que no te hace falta ninguno.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   $295. Lista en 72 horas.
DESCRIPCIÓN           El plazo cuenta desde tu material y la mitad del pago.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, me interesa el plan Start

──────────────── PIEZA 03 · 1080×1920 ────────────────
FONDO
Un proyectil de obsidiana pulida entrando en el cuadro desde arriba a velocidad
extrema, con las estelas de luz estirándose detrás de él hacia el borde
superior. La superficie del proyectil refleja sus propias estelas y la forma es
aerodinámica y sin marcas, como una gota de piedra negra. [BLOQUE DE ESTILO]
[ENCUADRE 9:16] [NEGATIVOS]

ANTETÍTULO   PANACLAW START
TITULAR      Antonio 700, 112 px, tres líneas, centro óptico y=880
             ABRE EN MENOS
             DE UN SEGUNDO.
             >>>TE LO MIDO DELANTE.<<<
CIFRA        $295
NOTA         72 HORAS DESDE TU MATERIAL Y LA MITAD DEL PAGO. LOS CAMBIOS LOS
             HAGO YO: ME ESCRIBES Y LO CAMBIO.

TEXTO PRINCIPAL
Tu página tarda y la gente se va antes de ver lo que vendes. $295, lista en 72
horas.
Abre en menos de un segundo, en el celular y en la computadora, y te lo mido
delante el primer día. No hay complementos que actualizar cada semana ni panel
público por el que alguien pueda entrar.
En Start los cambios los hago yo: me escribes y lo cambio. Si quieres editarlo
tú mismo, eso es Corporate, $850.
Escríbeme por WhatsApp y te digo cuál te encaja, o que no te hace falta ninguno.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   Abre en menos de un segundo
DESCRIPCIÓN           $295, lista en 72 horas.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, me interesa el plan Start

──────────────── PIEZA 04 · 1080×1350 ────────────────
FONDO
Una retícula infinita de servidores negros encendidos en rojo, perdiéndose
hacia el horizonte en filas perfectamente alineadas. Uno solo, en primer plano,
arde más fuerte que los demás. [BLOQUE DE ESTILO] [ENCUADRE 4:5] [NEGATIVOS]

ANTETÍTULO   PANACLAW START
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=594
             NADIE TE PUEDE
             QUITAR TU PÁGINA.
             >>>NI YO.<<<
CIFRA        $295
NOTA         EL CÓDIGO Y LA DIRECCIÓN EN INTERNET QUEDAN A TU NOMBRE AL PAGO
             FINAL. ESTÁ EN EL CONTRATO.

TEXTO PRINCIPAL
Tu página la registró la agencia a su nombre y el día que quieras irte, empiezas
de cero. $295, lista en 72 horas.
Lo normal aquí es que la agencia se quede el dominio, el alojamiento y el
código, y que enterarte te cueste otra web entera. Al pago final todo pasa a
una cuenta tuya, y eso está en el contrato, no en mi palabra.
No incluye escribir tus textos ni una sesión de fotos. Te ayudo a ordenar lo
que ya tienes mientras hablamos.
Escríbeme por WhatsApp y te digo cuál te encaja, o que no te hace falta ninguno.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   El código y el dominio, a tu nombre
DESCRIPCIÓN           $295, lista en 72 horas.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, me interesa el plan Start

──────────────── PIEZA 05 · 1080×1920 ────────────────
FONDO
Una esfera de roca incandescente vista de cerca y desde abajo. Las grietas de
su superficie se abren en filamentos encendidos y el resto de la cámara ha
desaparecido en negro. [BLOQUE DE ESTILO] [ENCUADRE 9:16] [NEGATIVOS]

ANTETÍTULO   PANACLAW START
TITULAR      Antonio 700, 112 px, tres líneas, centro óptico y=880
             LO QUE NO ENTRA
             ESTÁ PUBLICADO
             >>>AL LADO DEL PRECIO.<<<
CIFRA        $295
NOTA         START NO LLEVA RONDAS DE CAMBIOS. SI DESPUÉS QUIERES CAMBIAR ALGO
             SE PIDE Y YA ESTÁ: $40, SABIDO DE ANTEMANO.

TEXTO PRINCIPAL
Lo que no entra está publicado al lado del precio, no en la tercera reunión.
$295, lista en 72 horas.
Start no lleva rondas de cambios. Si después se te ocurre algo, se pide y ya
está: $40, sin discusión y sin mala cara, y lo sabes desde antes de empezar.
Tampoco lleva panel para editar tú mismo: me escribes y lo cambio yo. Si
quieres hacerlo tú, eso es Corporate, $850.
Escríbeme por WhatsApp y te digo cuál te encaja, o que no te hace falta ninguno.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   $295. Lo que no entra, publicado
DESCRIPCIÓN           Ronda extra $40, sabida de antemano.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, me interesa el plan Start

──────────────── PIEZA 06 · 1080×1350 ────────────────
FONDO
Un proyectil de obsidiana pulida atravesando el cuadro de izquierda a derecha,
con las estelas de luz roja estirándose muy largas detrás de él. La forma es
aerodinámica y sin marcas, como una gota de piedra negra, y el aire alrededor
está completamente oscuro. [BLOQUE DE ESTILO] [ENCUADRE 4:5] [NEGATIVOS]

ANTETÍTULO   DIAGNÓSTICO DE VENTAS
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=594
             TU SITIO TARDA
             Y LA GENTE SE VA
             >>>ANTES DE VERLO.<<<
CIFRA        $49
NOTA         INFORME Y LLAMADA DE 30 MINUTOS EN 48 HORAS. DICE QUÉ ESTÁ MAL Y
             QUÉ HACER; ARREGLARLO SE COTIZA APARTE.

TEXTO PRINCIPAL
Tu sitio tarda y la gente se va antes de verlo. $49 y en 48 horas sabes por qué.
Cuatro de cada diez personas abandonan una página que tarda más de tres
segundos. Es un dato del sector, no una medición mía: lo tuyo lo mido y te digo
cuánto tarda de verdad.
El informe trae las tres razones concretas por las que estás perdiendo ventas y
qué hacer con cada una. Arreglarlo se cotiza aparte, y para entonces ya sabrás
exactamente qué estás arreglando y por qué.
Escríbeme por WhatsApp y te digo si vale la pena o si no me necesitas.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   $49. Informe en 48 horas.
DESCRIPCIÓN           Tres razones concretas, y qué hacer con cada una.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, quiero el Diagnóstico de Ventas

──────────────── PIEZA 07 · 1080×1350 ────────────────
FONDO
Tres cintas de luz roja trenzándose sobre una superficie de obsidiana pulida.
Las cintas se cruzan en un solo punto del cuadro y ahí la luz se concentra;
hacia los bordes se separan y se apagan. [BLOQUE DE ESTILO] [ENCUADRE 4:5]
[NEGATIVOS]

ANTETÍTULO   DIAGNÓSTICO DE VENTAS
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=594
             >>>TRES RAZONES<<<
             POR LAS QUE TU
             SITIO NO VENDE.
CIFRA        $49
NOTA         INFORME Y LLAMADA DE 30 MINUTOS EN 48 HORAS. SE PAGA ENTERO POR
             ADELANTADO PORQUE SE ENTREGA EN DOS DÍAS.

TEXTO PRINCIPAL
Tienes sitio, va mal, y nadie te ha dicho por qué. $49, informe y llamada en 48
horas.
Tres razones concretas por las que estás perdiendo ventas en él, y qué hacer
con cada una. Con datos delante, no con una opinión.
Se paga entero por adelantado porque se entrega en dos días. No incluye
arreglar nada: eso se cotiza aparte y ya sabrás exactamente qué estás
arreglando y por qué.
Escríbeme por WhatsApp y te digo si vale la pena o si no me necesitas.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   Tres razones. $49.
DESCRIPCIÓN           Informe y llamada de 30 minutos en 48 horas.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, quiero el Diagnóstico de Ventas

──────────────── PIEZA 08 · 1080×1920 ────────────────
FONDO
Una columna de servidores negros con vetas rojas alzándose desde abajo hacia el
borde superior del cuadro, vista desde el suelo. Las filas se repiten hacia
arriba hasta perderse en la oscuridad. [BLOQUE DE ESTILO] [ENCUADRE 9:16]
[NEGATIVOS]

ANTETÍTULO   PANACLAW START
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=880
             LA DIRECCIÓN
             EN INTERNET
             >>>ES TUYA,<<< NO MÍA.
CIFRA        $295
NOTA         EL DOMINIO SE REGISTRA A TU NOMBRE. RENOVARLO CUESTA UNOS $15 AL
             AÑO Y ES LO ÚNICO QUE SIGUE COSTANDO CADA AÑO.

TEXTO PRINCIPAL
La dirección de tu negocio en internet la tiene tu proveedor, no tú. $295, lista
en 72 horas.
El dominio se registra a tu nombre y el código pasa a una cuenta tuya al pago
final. Te puedes llevar todo sin pedirme permiso, y esa es la idea.
Renovar el dominio cuesta unos $15 al año y es lo único que sigue costando cada
año. El mantenimiento es aparte y es opcional: muchos no lo contratan y el sitio
funciona igual.
Escríbeme por WhatsApp y te digo cuál te encaja, o que no te hace falta ninguno.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   La dirección en internet es tuya
DESCRIPCIÓN           $295, lista en 72 horas.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, me interesa el plan Start

──────────────── PIEZA 09 · 1080×1350 ────────────────
FONDO
Tres bloques de cristal rojo encajándose uno dentro de otro, vistos desde
arriba y de cerca. El tercero todavía no ha terminado de entrar y la junta
abierta deja escapar luz. [BLOQUE DE ESTILO] [ENCUADRE 4:5] [NEGATIVOS]

ANTETÍTULO   DIAGNÓSTICO DE VENTAS
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=594
             >>>EN 48 HORAS<<<
             SABES QUÉ LE
             PASA A TU WEB.
CIFRA        $49
NOTA         INFORME Y LLAMADA DE 30 MINUTOS. SE PAGA ENTERO POR ADELANTADO
             PORQUE SE ENTREGA EN DOS DÍAS.

TEXTO PRINCIPAL
Se te cayó una vez, nadie supo por qué, y sigues sin saberlo. En 48 horas lo
sabes. $49.
El informe llega con las tres razones concretas por las que estás perdiendo
ventas, y una llamada de 30 minutos para explicártelas.
Mira el negocio: por qué no vende. Por dónde te pueden entrar lo mira la
Auditoría de Seguridad, que es otro trabajo y otro precio, y te digo cuál de
los dos te toca antes de que pagues ninguno.
Escríbeme por WhatsApp y te digo si vale la pena o si no me necesitas.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   $49. Informe y llamada en 48 h
DESCRIPCIÓN           Tres razones concretas, y qué hacer con cada una.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, quiero el Diagnóstico de Ventas

──────────────── PIEZA 10 · 1080×1350 ────────────────
FONDO
El morro de un proyectil de obsidiana pulida, muy cerca, con las estelas de luz
roja naciendo justo detrás del borde y perdiéndose fuera de cuadro. El resto
del proyectil se disuelve en negro. [BLOQUE DE ESTILO] [ENCUADRE 4:5]
[NEGATIVOS]

ANTETÍTULO   DIAGNÓSTICO DE VENTAS
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=594
             EL CLIC LO PAGAS
             TÚ. LA ESPERA
             >>>LA PAGAN ELLOS.<<<
CIFRA        $49
NOTA         INFORME Y LLAMADA DE 30 MINUTOS EN 48 HORAS. MIRA POR QUÉ NO
             VENDE, NO POR DÓNDE TE PUEDEN ENTRAR.

TEXTO PRINCIPAL
Pagas el clic y la página donde cae tarda. El clic lo pagas tú; la espera la
pagan ellos. $49.
Cuatro de cada diez personas abandonan una página que tarda más de tres
segundos: es un dato del sector, no una medición mía. Lo que sí mido es la tuya,
y te digo cuánto tarda de verdad.
Informe y llamada de 30 minutos en 48 horas. Mira por qué no vende, no por dónde
te pueden entrar: eso es la Auditoría de Seguridad y es otro trabajo.
Escríbeme por WhatsApp y te digo si vale la pena o si no me necesitas.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   $49. Cuánto tarda de verdad
DESCRIPCIÓN           Informe y llamada de 30 minutos en 48 horas.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, quiero el Diagnóstico de Ventas

──────────────── PIEZA 11 · 1080×1920 ────────────────
FONDO
Una cinta de luz roja separándose de otras dos sobre obsidiana pulida, vista muy
de cerca. El punto donde se despega es lo más brillante del cuadro; el resto se
apaga hacia abajo. [BLOQUE DE ESTILO] [ENCUADRE 9:16] [NEGATIVOS]

ANTETÍTULO   DIAGNÓSTICO DE VENTAS
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=880
             TE DIGO >>>DÓNDE
             SE TE ESCAPAN<<<
             LOS CLIENTES.
CIFRA        $49
NOTA         INFORME Y LLAMADA DE 30 MINUTOS EN 48 HORAS. NO INCLUYE
             ARREGLARLO: ESO SE COTIZA APARTE.

TEXTO PRINCIPAL
Sabes lo que te cuesta un clic. Nadie te ha dicho qué te cuesta la página donde
cae. $49.
El precio está publicado, es el mismo para todos y no hay descuento, y esa es la
idea. Lo que te llevas: las tres razones concretas por las que se te escapan los
clientes, y qué hacer con cada una.
Informe y llamada de 30 minutos en 48 horas. No incluye arreglarlo: eso se
cotiza aparte y ya sabrás exactamente qué estás pagando.
Escríbeme por WhatsApp y te digo si vale la pena o si no me necesitas.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   $49. El mismo precio para todos
DESCRIPCIÓN           Informe y llamada de 30 minutos en 48 horas.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, quiero el Diagnóstico de Ventas

──────────────── PIEZA 12 · 1080×1350 ────────────────
FONDO
Dos proyectiles de obsidiana pulida cruzando el cuadro a distinta altura,
vistos desde abajo. Uno deja una estela larga y encendida; el otro apenas
arrastra un rastro que se está apagando. [BLOQUE DE ESTILO] [ENCUADRE 4:5]
[NEGATIVOS]

ANTETÍTULO   DIAGNÓSTICO DE VENTAS
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=594
             >>>DOS DÍAS<<< Y SABES
             SI VALE LA PENA
             ARREGLARLA.
CIFRA        $49
NOTA         INFORME Y LLAMADA DE 30 MINUTOS EN 48 HORAS. TE DIGO SI TIENE
             ARREGLO O SI SALE MEJOR HACERLA DE NUEVO.

TEXTO PRINCIPAL
Llevas meses mandando gente a una página que no te trae clientes. En dos días
sabes si tiene arreglo. $49.
El informe trae las tres razones concretas por las que estás perdiendo ventas y
qué hacer con cada una, más una llamada de 30 minutos para explicarlo.
Y si sale mejor hacerla de nuevo, te lo digo, aunque la respuesta sea que no me
necesitas para lo que estabas pensando.
Escríbeme por WhatsApp y lo miramos.
El fondo de esta imagen está generado con inteligencia artificial.

TITULAR DEL ANUNCIO   $49. En dos días lo sabes.
DESCRIPCIÓN           Informe y llamada de 30 minutos en 48 horas.
BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, quiero el Diagnóstico de Ventas

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
8. ANTES DE DEVOLVER, COMPRUEBA
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

No escribiste, redactaste, completaste, acortaste, tradujiste ni "mejoraste"
ningún texto. Todo lo que aparece en el documento está copiado carácter por
carácter de lo que te di, con sus tildes, sus eñes y sus puntos finales.

  [ ] ¿Añadiste alguna cifra, porcentaje, estadística, plazo o beneficio que
      no estuviera escrito arriba? Quítalo.
  [ ] ¿Hay un solo emoji, un solo signo de exclamación o una sola palabra en
      mayúsculas de énfasis? Quítalo.
  [ ] ¿Algún fondo generado tiene letras, cifras, iconos, logotipos o
      gráficos dentro? Regenéralo.
  [ ] ¿Aparece azul, cian, verde, morado, amarillo, rosa, pastel, blanco puro
      o algún degradado multicolor en algún fondo? Regenéralo.
  [ ] ¿Aparece alguna persona, rostro, mano humana, silueta, oficina, laptop
      o pantalla? Regenéralo.
  [ ] ¿#FF1E1E toca alguna letra? Solo puede estar en la imagen de fondo.
  [ ] ¿Hay más de un tramo naranja en algún titular?
  [ ] ¿Las marcas >>> y <<< se imprimieron en alguna pieza? No deben verse.
  [ ] ¿Cada titular es Antonio 700 en versalitas y todo lo demás es Archivo?
      Ninguna otra familia, en ningún caso.
  [ ] ¿Los cortes de línea son exactamente los que te di?
  [ ] ¿El orden del bloque es antetítulo, titular, cifra, nota, en las doce?
  [ ] ¿Hay alguna caja, franja, tarjeta o sombra detrás de algún texto?
  [ ] ¿El wordmark dice PANACLAW en #FFF7F7 con el punto final en #FF5100?
  [ ] ¿El símbolo lleva fill-rule="evenodd" y conserva su proporción
      100 × 81.56, sin estirar?
  [ ] ¿Las ocho piezas 4:5 exportan a 1080×1350 exactos y las cuatro 9:16 a
      1080×1920 exactos?
  [ ] ¿Están las cinco trampas del exportador resueltas, en particular el
      reinicio de ctx.letterSpacing a '0px' y ctx.textBaseline='top'?
````

---

## PARTE 3 · Qué comprobar cuando devuelva el documento

1. **Descarga una pieza y ponla al lado de su vista previa.** Si no son
   idénticas, el exportador está mal, y si está mal en una está mal en las doce.
   Un desfase de dos o tres píxeles es normal; por encima de seis, algo está mal
   calculado.
2. **Mira la banda del símbolo** (y 96 a 168 en las 4:5, y 312 a 384 en las
   9:16). Si asoma resplandor, forma o reflejo del fondo, **se regenera el
   fondo**. No se tapa con más velo: se probó y la mejora es insuficiente.
3. **Lee un texto cualquiera contra este archivo**, palabra por palabra. El
   fallo más frecuente de Meta AI es reescribir una frase que suena parecida y
   añadir una cifra que nadie le dio.
4. **Cuenta las cifras.** Solo pueden aparecer: `$295`, `$49`, `$40`, `$850`,
   `$15 al año`, `72 horas`, `48 horas`, `30 minutos`, `tres razones`,
   `cuatro de cada diez` y `tres segundos`.
5. **Mira qué fuentes cargó de verdad.** El prompt maestro solo declara las dos
   permitidas y no lista las prohibidas, para no meter en el pegado una lista de
   familias que no deben aparecer. La lista completa, con el porqué, está en
   `datos/marca.json` → `redesSociales.tipografia.prohibidas`. Si el documento
   cae a una fuente del sistema, la pieza deja de ser de la marca aunque el
   resto esté bien.

---

## PARTE 4 · Lo que este entregable NO incluye

- **No hay vídeo.** `campanas/canales/meta.md` recomienda un reparto de 70 %
  vídeo y 30 % imagen, y esta campaña es 100 % imagen. El motivo está en
  `operacion/deuda-conocida.md`: hay estructura de guion en
  `prompts/video/video-corto.md` pero **no hay cadena de producción de vídeo**
  equivalente a la de imagen. Fingir el 70/30 sería peor que decirlo. Los cuatro
  creativos 9:16 sí ocupan la ubicación de Reels, que es donde está el coste por
  clic bajo.
- **No hay prueba social.** Ni testimonios, ni métricas por proyecto, ni número
  de clientes, ni logos: nada de eso está verificado hoy
  (`catalogo/09-prueba.md`). Su lugar lo ocupan las promesas comprobables el
  primer día: abre en menos de un segundo, el código y el dominio quedan a tu
  nombre, el precio y las exclusiones están publicados.
- **No hay campaña de remarketing todavía.** El píxel tiene que acumular
  visitantes primero. Cuando los tenga, los públicos y qué anunciarle a cada uno
  están en `campanas/canales/meta.md`.
- **No hay campaña de Google.** Se puede correr pero no leer: falta configurar
  Google Analytics 4.
- **No se anuncia el sitio.** Los doce anuncios van a WhatsApp mientras el sitio
  siga en un subdominio prestado.

---

## PARTE 5 · Decisiones que el dueño de la marca podría querer distintas

1. **Los creativos llevan el texto compuesto dentro de la imagen.**
   `campanas/plantillas/estructura-anuncio.md` pone «texto en imagen» por
   defecto en «no». Aquí va en «sí»: en frío, sin seguidores y compitiendo con
   todo el feed, el titular dentro de la pieza es lo que detiene el pulgar, y el
   sistema visual de la marca está construido exactamente para sostener un
   titular. El copy completo va igualmente en los campos del editor de anuncios.
   Si se prefiere el defecto, se quitan las capas de texto y quedan doce fondos.
2. **La retícula de 1080×1920 está derivada, no copiada.** `datos/marca.json`
   declara el lienzo de story y dice que los márgenes laterales no cambian y que
   los anclajes verticales se recalculan, pero **no publica los valores
   recalculados**. Los de este entregable —símbolo en y=312, centro óptico en
   y=880, wordmark con base en y=1500— son un cálculo hecho aquí contra las
   zonas seguras del 15 % y el 20 %. Si se aprueban, su sitio es
   `datos/marca.json` → `redesSociales.reticula`, no este archivo.
3. **El presupuesto está por debajo del rango documentado.** $15 al día
   funciona, pero tarda: el mismo gasto que produce datos legibles en 5–7 días a
   $20–50 diarios tarda de 7 a 10 a este ritmo. La alternativa no es repartirlo <!-- v: rango de presupuesto diario de campanas/canales/meta.md, no un precio del catálogo -->
   mejor, es esperar más antes de leer nada.
