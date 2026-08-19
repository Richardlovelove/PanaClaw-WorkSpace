# Entregable · Campaña Meta de arranque · 2026-08

> **Esto no es doctrina del repositorio.** Es un entregable con fecha, revisado
> el 2026-08-19. Cuando la campaña termine, este archivo **se borra** — la regla
> de este repositorio es que no se guardan copys finales (`CLAUDE.md` §7). Lo que
> sí se queda, si algo de aquí se aprueba como norma, sube a `datos/`,
> `campanas/` o `prompts/` por la vía de `operacion/sincronizacion.md`.

Presupuesto: **$15 al día**. Página de Facebook, cuenta de Instagram y dos
semanas de contenido orgánico programado, a las 8:00 y a las 11:00 todos los
días. Sitio web publicado con el píxel de Meta puesto.

---

## PARTE 0 · Qué queda por resolver antes de subir

De los cuatro puntos que bloqueaban la versión anterior, **dos se cayeron**:
la página de Facebook, la cuenta de Instagram y el contenido ya existen. Quedan
dos, y los dos se hacen dentro del editor de anuncios, no antes.

| Qué | Por qué | Cuándo |
|---|---|---|
| **Declarar contenido generado con IA** en los 12 anuncios | Meta lo exige desde marzo de 2026 y no declararlo es de los motivos de rechazo más frecuentes. Todos los fondos de esta marca los genera un motor de imagen | Al crear cada anuncio |
| **Desactivar las mejoras automáticas de creativo** | Reencuadran, filtran y cambian el color. Con un fondo `#100101` y un solo acento `#FF5100`, cualquier ajuste automático rompe la pieza | En el conjunto, antes de publicar |

Y una comprobación de un minuto: **que WhatsApp Business esté conectado a la
página de Facebook**. Sin eso el objetivo de mensajes no ofrece WhatsApp como
destino, y esta campaña entera cuelga de ahí.

---

## PARTE 1 · La decisión: a dónde va el clic

Es la pregunta que hay que contestar antes de cualquier otra cosa, porque cambia
el objetivo, el evento y el copy de los doce anuncios.

### La respuesta: WhatsApp, en los doce. El sitio no recibe pauta todavía.

**No es porque el sitio esté mal.** Es aritmética de arranque.

Un conjunto necesita unas 50 conversiones semanales del evento que optimiza para
salir de la fase de aprendizaje. Con $15 al día son $105 a la semana. **Cincuenta <!-- v: $105 es 15 × 7, aritmética de presupuesto de pauta, no un precio del catálogo -->
eventos sobre $105 exigen que cada uno cueste $2.10 o menos.** <!-- v: $2.10 es 105 ÷ 50, el techo de coste por evento, no un precio del catálogo -->

- Un envío de formulario del sitio **no cuesta eso en ningún mercado**. Optimizar
  contra `Lead` a este presupuesto es apostar el dinero a un número que nadie ha
  medido, y el conjunto se queda en aprendizaje limitado: lo que se lea después
  es ruido.
- Una conversación de WhatsApp **sí puede costar eso**. Es el evento más barato
  y más frecuente que la marca puede comprar hoy.
- Y es donde la marca cierra de verdad. No se está inventando un embudo para la
  campaña: se está pagando por llenar el que ya existe.

### Qué hace el sitio mientras tanto

No se queda parado. Hace tres cosas, y ninguna necesita presupuesto:

1. **Acumula píxel** con el tráfico orgánico de las dos semanas programadas. Eso
   es exactamente el público que hace posible la campaña de remarketing.
2. **Es lo que se manda dentro de la conversación de WhatsApp**, que es donde ya
   hay intención. Ahí el enlace lo abre alguien que preguntó, no alguien a quien
   se le interrumpió.
3. **Es el destino de la campaña 2**, cuando la haya.

### Cuándo sí se le manda pauta al sitio

Cuando se cumplan las dos:

- El píxel tiene público suficiente para que Meta deje de marcar el público de
  remarketing como demasiado pequeño.
- Hay dominio propio. Un anuncio pagado que cae en un subdominio prestado
  contradice «el sitio es tuyo» en el primer clic, y es lo primero que nota
  alguien que está evaluando agencias (`operacion/deuda-conocida.md` §1).

> **Supuesto declarado:** doy por hecho que el sitio sigue en
> `panaclaw.netlify.app`. Si ya está en dominio propio, dilo y la fase 2 puede
> arrancar en cuanto el píxel tenga público — la fase 1 no cambia de todos
> modos.

### Lo que NO se hace

**No se promociona ninguna publicación orgánica.** El botón de promocionar crea
una campaña paralela que compite por el mismo público con el mismo dinero, y no
deja elegir el evento contra el que optimiza. Con $15 al día, todo va a un solo <!-- v: presupuesto diario del cliente, no un precio del catálogo -->
conjunto o no aprende ninguno.

---

## PARTE 2 · La ficha de campaña

Esto es lo que va copiado dentro del documento HTML, para no tener que
escribirlo dos veces ni dejar que nadie lo invente.

```
NOMBRE DE CAMPAÑA
  PanaClaw · Arranque · Conversaciones · 2026-08

OBJETIVO
  Interacción, optimizado a conversaciones de mensajería.
  NO se optimiza contra Lead del píxel. El motivo, con los números, en
  campanas/canales/meta.md

APLICACIÓN DE DESTINO
  WhatsApp

PRESUPUESTO
  $15 al día, fijado a nivel de campaña
  Estrategia de puja: el coste más bajo, sin tope
  Calendario: continuo, sin fecha de fin

CONJUNTO DE ANUNCIOS — uno solo
  Nombre        PanaClaw · Panamá · Amplio 25–55
  Ubicación     Panamá
  Edad          25–55
  Género        Todos
  Idioma        Español
  Intereses     NINGUNO
  Ubicaciones   Automáticas
  Tope de cliente existente   entre 10 % y 20 %
  Públicos parecidos          no, todavía no hay eventos suficientes

ANUNCIOS — doce, todos dentro del mismo conjunto
  6  imagen única 4:5    1080×1350
  4  imagen única 9:16   1080×1920
  2  carrusel 4:5        tres tarjetas cada uno, 1080×1350

AUTOMATIZACIONES
  Público automático              aceptar
  Ubicaciones automáticas         aceptar
  Presupuesto automático          aceptar
  Mejoras automáticas de creativo DESACTIVAR
  Emojis sugeridos por Meta       rechazar
  Mejorar el copy con la IA de Meta   rechazar
  Recortar la imagen a otras proporciones   rechazar
  Botón de "Reservar ahora"       rechazar

DECLARACIÓN DE CONTENIDO GENERADO CON IA
  Activada en los doce anuncios

MEDICIÓN
  Píxel de Meta 1067898639025746, activo. Se queda encendido midiendo de
  fondo aunque no se optimice contra él: está acumulando el histórico que
  hace falta para pasar a Lead más adelante
  Evento que cuenta como éxito: conversación de mensajería iniciada
  Google Analytics 4: sin configurar. Google no se puede leer todavía

QUÉ SE LEE, Y CUÁNDO
  Conversaciones iniciadas y coste por conversación
  No antes de 7 a 10 días. Un ganador declarado con tres conversaciones es
  ruido
  Las subidas de presupuesto van del 20 % cada tres o cuatro días. Un salto
  mayor devuelve el conjunto a la fase de aprendizaje
  Renovar creativos cada dos o tres semanas, no cuando bajen los resultados

QUÉ NO SE MIDE, Y NO SE PROPONE
  Coste por cliente, tasa de conversión por canal, retorno de la inversión.
  Con un píxel y un evento, esas métricas no existen
```

### Los dos productos de entrada

Solo dos cifras del catálogo son lo bastante bajas para decidirse dentro de un
anuncio en frío:

| Producto | Precio | Plazo | Anuncios |
|---|---|---|---|
| PanaClaw Start | $295 | 72 h | 01, 02, 03, 04, 05, 08 |
| Diagnóstico de Ventas | $49 | Informe y llamada de 30 min en 48 h | 06, 07, 09, 10, 11, 12 |

Launch $450, Corporate $850, Commerce $1,200, eBot $499 y los planes de
seguridad **no se anuncian en frío**. Se venden dentro de la conversación de
WhatsApp, que es donde está el margen y donde se califica.

### Los 12 anuncios, en una vista

| # | Público | Producto | Ángulo (hipótesis) | Altura del titular | Formato | Escena madre |
|---|---|---|---|---|---|---|
| 01 | No tiene sitio | Start $295 | Precio publicado | Consecuencia | Imagen 4:5 | 7 · Esfera de roca |
| 02 | No tiene sitio | Start $295 | Plazo | Consecuencia | Imagen 4:5 | 3 · Hélice de cristal |
| 03 | No tiene sitio | Start $295 | Velocidad | Consecuencia | Imagen 9:16 | 1 · Proyectil |
| 04 | No tiene sitio | Start $295 | Propiedad | Consecuencia | Imagen 4:5 | 4 · Servidores |
| 05 | No tiene sitio | Start $295 | Precio publicado · qué entra y qué no | Consecuencia | **Carrusel 4:5, 3 tarjetas** | 7 · Esfera de roca |
| 06 | WordPress que da vergüenza | Diagnóstico $49 | Velocidad | Consecuencia | Imagen 4:5 | 1 · Proyectil |
| 07 | WordPress que da vergüenza | Diagnóstico $49 | Precio publicado · el entregable | Hecho | **Carrusel 4:5, 3 tarjetas** | 6 · Cintas de luz |
| 08 | No tiene sitio | Start $295 | Propiedad | Consecuencia | Imagen 9:16 | 4 · Servidores |
| 09 | WordPress que da vergüenza | Diagnóstico $49 | Plazo | Hecho | Imagen 9:16 | 3 · Hélice de cristal |
| 10 | Invierte en publicidad | Diagnóstico $49 | Velocidad | Consecuencia | Imagen 4:5 | 1 · Proyectil |
| 11 | Invierte en publicidad | Diagnóstico $49 | Precio publicado | Consecuencia | Imagen 9:16 | 6 · Cintas de luz |
| 12 | Invierte en publicidad | Diagnóstico $49 | Plazo | Hecho | Imagen 4:5 | 1 · Proyectil |

**Ángulos:** precio publicado 4 · plazo 3 · velocidad 3 · propiedad 2. Una
hipótesis por anuncio.
**Alturas de los doce titulares de apertura:** 9 consecuencia, 3 hecho, 0
condición. Dentro de los carruseles, una sola tarjeta abre por el límite —una de
dieciséis piezas, muy por debajo del tope de una de cada tres.
**Imágenes a generar:** 16 en total. Seis 4:5 sueltas, cuatro 9:16 sueltas y
seis tarjetas de carrusel.

**Lo que varía entre anuncios:** dolor, ángulo, escena madre y formato.
**Lo que no varía nunca:** el bloque de estilo, la paleta, el acento único y las
dos familias tipográficas. El motor de entrega agrupa creativos que se parecen y
los hace competir entre sí en vez de ampliar el alcance; la diversidad que cuenta
es de concepto y de formato, no de estilo.

---

## PARTE 3 · El prompt maestro

Se pega entero en Meta AI. Devuelve un documento HTML con la ficha de campaña
arriba, los 16 lienzos compuestos, descargables en PNG a tamaño real, y debajo de
cada anuncio su copy en texto seleccionable.

````
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. QUÉ ERES Y QUÉ NO HACES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Vas a hacer dos cosas y ninguna más: generar 16 fondos de imagen y montar un
documento HTML donde esos fondos se ven ya compuestos con su texto y se pueden
descargar.

No escribas, no redactes, no completes, no acortes, no traduzcas y no
"mejores" ningún texto. Todo el texto de este documento ya está escrito más
abajo: la ficha de campaña, los titulares, las notas y el copy de los doce
anuncios. Cópialo carácter por carácter, con sus tildes, sus eñes y sus puntos
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

RETÍCULA — lienzo 1080×1350 (formato 4:5: seis imágenes sueltas y las seis
tarjetas de carrusel)
  Margen lateral        72 izquierda, 1008 derecha. Ancho útil 936
  Todo alineado a la izquierda en x=72. El símbolo es la única excepción
  Símbolo               88 de ancho × 72 de alto, centrado horizontalmente,
                        caja de y=96 a y=168. EMPIEZA en 96, no está centrado
                        en 96. NO es cuadrado: proporción 100 × 81.56
  Bloque de texto       anclado por su centro óptico en y=594
  Wordmark              x=72, base del bloque en y=1254

RETÍCULA — lienzo 1080×1920 (formato 9:16, cuatro imágenes)
  Margen lateral        idéntico: 72 y 1008. Ancho útil 936
  Zonas seguras         nada de texto ni símbolo por encima de y=288 ni por
                        debajo de y=1536. Ahí caen la interfaz y los botones
  Símbolo               88 × 72, centrado, caja de y=312 a y=384
  Bloque de texto       anclado por su centro óptico en y=880
  Wordmark              x=72, base del bloque en y=1500

ESCALA — píxeles idénticos en los dos lienzos, porque los dos miden 1080 de
ancho
  Titular XL   Antonio 700, 132 px, interlínea 0.88, tracking -0.01em, #FFF7F7
  Titular L    Antonio 700, 112 px, interlínea 0.88, tracking -0.01em, #FFF7F7
  Antetítulo   Archivo 500, 24 px, tracking 0.16em, VERSALITAS, #FF5100,
               margen inferior 28
  Cifra        Antonio 700, 76 px, tracking 0, VERSALITAS, #FFF7F7,
               margen superior 44
  Nota         Archivo 400, 20 px, interlínea 1.5, tracking 0.14em,
               VERSALITAS, #BABABA, margen superior 28
  Wordmark     Archivo 700, 30 px, tracking 0.22em, VERSALITAS, #FFF7F7,
               con un punto final "." en #FF5100

  Titular y cifra siempre en versalitas. Cada pieza de abajo lleva escrito su
  tamaño de titular: úsalo, no lo recalcules.

EL ORDEN DEL BLOQUE DE TEXTO — no se negocia
  ANTETÍTULO
  TITULAR
  CIFRA
  NOTA

  La cifra va SIEMPRE después del titular, nunca antes. Si lo primero que se
  lee en una pieza es un número, está al revés. Ninguna de estas piezas lleva
  bajada, y algunas no llevan cifra: en esas, la nota va justo después del
  titular.

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

LOS DOS CARRUSELES
  Las tres tarjetas de un carrusel miden 1080×1350 las tres. No mezcles
  proporciones: deja bandas al deslizar.
  El anclaje del texto NO salta entre tarjetas: las tres van ancladas por su
  centro óptico en y=594.
  El símbolo y el wordmark van en las tres. Cada tarjeta se puede compartir
  suelta.
  La primera tarjeta lleva el peso: es la única que se ve en el feed sin
  deslizar.
  Numerador apagado.

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

Devuelve UN documento HTML completo, con las 16 imágenes dentro del propio
archivo, que se abra en el navegador sin depender de nada externo.

ESTRUCTURA DEL DOCUMENTO, DE ARRIBA ABAJO
  1. La ficha de campaña de la sección 4, copiada literal, en un panel al
     principio y en texto seleccionable. Es lo primero que se ve.
  2. Los doce anuncios, en orden, del 01 al 12.
  3. Un botón de descargar todo al final.

CADA ANUNCIO SE PRESENTA ASÍ
  - Un encabezado con su número, su formato, su público, su producto y su
     hipótesis, copiados literal de más abajo.
  - Su pieza o piezas compuestas. Los dos carruseles muestran sus tres
     tarjetas en fila, en el orden 1, 2, 3.
  - Debajo, en texto seleccionable para pegar en el editor de anuncios:
       Texto principal
       Titular del anuncio
       Descripción
       Botón
       Mensaje precargado de WhatsApp
       El prompt del fondo, por si hay que regenerar esa imagen
    En los carruseles, el titular y la descripción van por tarjeta.

FUENTES — sin esto todo lo demás da igual
  Carga Antonio y Archivo desde Google Fonts:
  https://fonts.googleapis.com/css2?family=Antonio:wght@700&family=Archivo:wght@300;400;500;700&display=swap
  Espera a document.fonts.ready antes de dibujar cualquier canvas.

CADA PIEZA, A MEDIDA REAL
  Las doce piezas 4:5 se dibujan a 1080×1350 exactos.
  Las cuatro piezas 9:16 se dibujan a 1080×1920 exactos.
  En pantalla se pueden ver reducidas con transform: scale(), pero el lienzo
  que se exporta mide exactamente eso.

BOTONES DE DESCARGA
  Cada pieza lleva su botón que la baja en PNG a tamaño real, dibujando la
  imagen y el texto sobre un <canvas> del tamaño que le toca. Sin librerías
  externas. Los archivos se nombran así: 01.png, 05a.png, 05b.png, 05c.png.
  Y un botón que las descargue todas.

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

  5. Un botón que lanza 16 descargas seguidas lo bloquea el navegador a la
     tercera. O agrupas en un ZIP de verdad, o el botón se llama "descargar
     una por una" y avisa de que hay que permitirlo.

LA INTERFAZ DEL DOCUMENTO
  Fondo #100101, texto #FFF7F7, acento #FF5100. Es una herramienta interna,
  pero se mira todo el mes.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
4. LA FICHA DE CAMPAÑA — cópiala literal en el panel del principio
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

NOMBRE DE CAMPAÑA
  PanaClaw · Arranque · Conversaciones · 2026-08

OBJETIVO
  Interacción, optimizado a conversaciones de mensajería.
  No se optimiza contra el evento Lead del píxel.

APLICACIÓN DE DESTINO
  WhatsApp

PRESUPUESTO
  15 dólares al día, fijado a nivel de campaña
  Estrategia de puja: el coste más bajo, sin tope
  Calendario: continuo, sin fecha de fin

CONJUNTO DE ANUNCIOS — uno solo
  Nombre                       PanaClaw · Panamá · Amplio 25-55
  Ubicación                    Panamá
  Edad                         25 a 55
  Género                       Todos
  Idioma                       Español
  Intereses                    Ninguno
  Ubicaciones                  Automáticas
  Tope de cliente existente    entre 10 y 20 por ciento
  Públicos parecidos           No. Todavía no hay eventos suficientes

ANUNCIOS — doce, todos dentro del mismo conjunto
  6  imagen única 4:5     1080 por 1350
  4  imagen única 9:16    1080 por 1920
  2  carrusel 4:5         tres tarjetas cada uno, 1080 por 1350

AUTOMATIZACIONES
  Público automático                        aceptar
  Ubicaciones automáticas                   aceptar
  Presupuesto automático                    aceptar
  Mejoras automáticas de creativo           desactivar
  Emojis sugeridos por Meta                 rechazar
  Mejorar el copy con la inteligencia artificial de Meta   rechazar
  Recortar la imagen a otras proporciones   rechazar
  Botón de Reservar ahora                   rechazar

DECLARACIÓN DE CONTENIDO GENERADO CON IA
  Activada en los doce anuncios. Todos los fondos los genera un motor de
  imagen y va declarado desde el primer día.

MEDICIÓN
  Píxel de Meta 1067898639025746, activo. Se queda encendido midiendo de
  fondo aunque no se optimice contra él.
  Evento que cuenta como éxito: conversación de mensajería iniciada.
  Google Analytics 4 sin configurar: Google no se puede leer todavía.

QUÉ SE LEE, Y CUÁNDO
  Conversaciones iniciadas y coste por conversación.
  No antes de 7 a 10 días. Un ganador declarado con tres conversaciones es
  ruido.
  Las subidas de presupuesto van del 20 por ciento cada tres o cuatro días.
  Un salto mayor devuelve el conjunto a la fase de aprendizaje.
  Renovar creativos cada dos o tres semanas.

QUÉ NO SE MIDE
  Coste por cliente, tasa de conversión por canal, retorno de la inversión.
  Con un píxel y un evento, esas métricas no existen.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
5. EL BLOQUE DE ESTILO — idéntico en las 16, palabra por palabra
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
6. LOS NEGATIVOS — idénticos en las 16, palabra por palabra
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

No incluyas: personas, oficinas, laptops ni pantallas; ningún azul, verde,
morado ni tono pastel; nada de blanco puro ni fondos claros; nada de luz
natural ni exteriores; ningún texto, letra, número, icono, logotipo ni
gráfico; nada de estética de stock corporativo; nada de candados, escudos,
bombillas, engranajes ni gráficos de barras.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
7. LOS DOS ENCUADRES — se pegan al final del prompt de cada fondo
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ENCUADRE 4:5 (piezas 01, 02, 04, 05a, 05b, 05c, 06, 07a, 07b, 07c, 10, 12)
Encuadre: composición vertical 4:5. Los 180 píxeles superiores y los 160
inferiores del cuadro quedan en negro limpio, sin ninguna forma, resplandor
ni reflejo, ni siquiera difuso. El sujeto vive entre esas dos bandas y se
abre hacia los bordes laterales y hacia el tercio superior. La banda central
del cuadro queda en negro limpio, con la incandescencia muriendo antes de
entrar en ella.

ENCUADRE 9:16 (piezas 03, 08, 09, 11)
Encuadre: composición vertical 9:16. Los 420 píxeles superiores y los 480
inferiores del cuadro quedan en negro limpio, sin ninguna forma, resplandor
ni reflejo, ni siquiera difuso. El sujeto vive entre esas dos bandas y se
abre hacia los bordes laterales. La banda central del cuadro, entre 590 y
1170 píxeles de altura, queda en negro limpio, con la incandescencia
apagándose antes de llegar a ella.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
8. LOS DOCE ANUNCIOS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

════════ ANUNCIO 01 · imagen única 4:5 · 1080×1350 ════════
Público: el que no tiene sitio · Producto: PanaClaw Start
Hipótesis: le duele que nadie le dé una cifra

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

════════ ANUNCIO 02 · imagen única 4:5 · 1080×1350 ════════
Público: el que no tiene sitio · Producto: PanaClaw Start
Hipótesis: le duele la espera

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

════════ ANUNCIO 03 · imagen única 9:16 · 1080×1920 ════════
Público: el que no tiene sitio · Producto: PanaClaw Start
Hipótesis: le duele que su página sea lenta

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

════════ ANUNCIO 04 · imagen única 4:5 · 1080×1350 ════════
Público: el que no tiene sitio · Producto: PanaClaw Start
Hipótesis: le duele depender de quien se la hizo

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

════════ ANUNCIO 05 · CARRUSEL 4:5 · tres tarjetas · 1080×1350 cada una ════════
Público: el que no tiene sitio · Producto: PanaClaw Start
Hipótesis: le duele no saber qué entra y qué no hasta que ya pagó
Las tres tarjetas van ancladas por su centro óptico en y=594. No salta.

──── TARJETA 05a ────
FONDO
Una esfera de roca incandescente flotando sola en el centro de una cámara de
piedra negra, vista de lejos. La cámara se pierde en la oscuridad y solo los
muros más cercanos reciben algo de resplandor. [BLOQUE DE ESTILO]
[ENCUADRE 4:5] [NEGATIVOS]

ANTETÍTULO   PANACLAW START
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=594
             TE DIGO LO QUE
             NO ENTRA ANTES
             >>>DE COBRARTE.<<<
CIFRA        $295
NOTA         72 HORAS DESDE QUE ME DAS TU MATERIAL Y LA MITAD DEL PAGO.

TITULAR DE LA TARJETA   $295. Lista en 72 horas.
DESCRIPCIÓN             El precio y lo que no entra, los dos publicados.

──── TARJETA 05b ────
FONDO
La misma esfera de roca incandescente, ahora a media distancia. Se distinguen
las vetas encendidas que recorren su superficie y la cámara sigue disolviéndose
en negro alrededor. [BLOQUE DE ESTILO] [ENCUADRE 4:5] [NEGATIVOS]

ANTETÍTULO   QUÉ ENTRA
TITULAR      Antonio 700, 112 px, cuatro líneas, centro óptico y=594
             CUATRO O CINCO
             SECCIONES Y LOS
             MENSAJES >>>TE LLEGAN
             AL WHATSAPP.<<<
NOTA         PUBLICACIÓN INCLUIDA Y MEDICIÓN DE VISITAS INCLUIDA. NO HAY QUE
             PAGAR NADA APARTE PARA QUE QUEDE ABIERTA EN INTERNET.

TITULAR DE LA TARJETA   Qué entra en Start
DESCRIPCIÓN             Cuatro o cinco secciones, publicación incluida.

──── TARJETA 05c ────
FONDO
Un plano muy cercano de la superficie de la esfera de roca incandescente. Las
grietas se abren en filamentos encendidos y todo lo demás ha desaparecido en
negro. [BLOQUE DE ESTILO] [ENCUADRE 4:5] [NEGATIVOS]

ANTETÍTULO   QUÉ NO ENTRA
TITULAR      Antonio 700, 112 px, cuatro líneas, centro óptico y=594
             SIN PANEL PARA
             EDITAR TÚ MISMO.
             >>>ME ESCRIBES
             Y LO CAMBIO YO.<<<
NOTA         START NO LLEVA RONDAS DE CAMBIOS Y LA EXTRA CUESTA $40, SABIDA DE
             ANTEMANO. SI QUIERES EDITARLO TÚ, ESO ES CORPORATE, $850.

TITULAR DE LA TARJETA   Qué no entra
DESCRIPCIÓN             Ronda extra $40. Editar tú mismo es Corporate.

TEXTO PRINCIPAL DEL ANUNCIO 05
Lo que no entra está publicado al lado del precio, no en la tercera reunión.
$295, lista en 72 horas.
Start son cuatro o cinco secciones, los mensajes te llegan al WhatsApp y la
publicación va incluida: queda abierta en internet sin que pagues nada aparte.
Lo que no lleva: rondas de cambios, y panel para editar tú mismo. Si después se
te ocurre algo, se pide y ya está, $40, sin discusión. Y si quieres cambiarlo tú
desde el celular, eso es Corporate, $850.
Escríbeme por WhatsApp y te digo cuál te encaja, o que no te hace falta ninguno.
Los fondos de estas imágenes están generados con inteligencia artificial.

BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, me interesa el plan Start

════════ ANUNCIO 06 · imagen única 4:5 · 1080×1350 ════════
Público: el que tiene un WordPress que le da vergüenza · Producto: Diagnóstico
de Ventas
Hipótesis: le duele que su sitio sea lento y no saber por qué

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

════════ ANUNCIO 07 · CARRUSEL 4:5 · tres tarjetas · 1080×1350 cada una ════════
Público: el que tiene un WordPress que le da vergüenza · Producto: Diagnóstico
de Ventas
Hipótesis: le duele que nadie le explique qué le pasa a su sitio
Las tres tarjetas van ancladas por su centro óptico en y=594. No salta.

──── TARJETA 07a ────
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

TITULAR DE LA TARJETA   $49. Informe en 48 horas.
DESCRIPCIÓN             Tres razones concretas, y qué hacer con cada una.

──── TARJETA 07b ────
FONDO
Dos de esas cintas de luz roja vistas a media distancia sobre la obsidiana
pulida, con una tercera entrando desde el borde. El cruce queda fuera de cuadro
y lo que se ve es el recorrido. [BLOQUE DE ESTILO] [ENCUADRE 4:5] [NEGATIVOS]

ANTETÍTULO   LO PRIMERO QUE MIDO
TITULAR      Antonio 700, 112 px, tres líneas, centro óptico y=594
             PRIMERO TE DIGO
             >>>CUÁNTO TARDA
             DE VERDAD<<< EN ABRIR.
NOTA         MEDIDO, CON LA FECHA PUESTA. NO ES UN DATO DEL SECTOR NI UNA
             ESTIMACIÓN.

TITULAR DE LA TARJETA   Cuánto tarda de verdad
DESCRIPCIÓN             Medido, con la fecha puesta.

──── TARJETA 07c ────
FONDO
Una sola cinta de luz roja separándose de las otras sobre obsidiana pulida,
vista de cerca. El punto donde se despega es lo más brillante del cuadro y el
resto se apaga hacia los bordes. [BLOQUE DE ESTILO] [ENCUADRE 4:5] [NEGATIVOS]

ANTETÍTULO   Y SI NO ME NECESITAS
TITULAR      Antonio 700, 112 px, tres líneas, centro óptico y=594
             Y SI SALE MEJOR
             HACERLA DE NUEVO,
             >>>TE LO DIGO IGUAL.<<<
NOTA         NO INCLUYE ARREGLARLO: ESO SE COTIZA APARTE Y YA SABRÁS
             EXACTAMENTE QUÉ ESTÁS PAGANDO Y POR QUÉ.

TITULAR DE LA TARJETA   Te digo si no me necesitas
DESCRIPCIÓN             No incluye arreglarlo: eso se cotiza aparte.

TEXTO PRINCIPAL DEL ANUNCIO 07
Tienes sitio, va mal, y nadie te ha dicho por qué. $49, informe y llamada en 48
horas.
Lo primero es medirlo: cuánto tarda en abrir de verdad, con la fecha puesta, no
un dato del sector. Después, las tres razones concretas por las que estás
perdiendo ventas en él y qué hacer con cada una.
Se paga entero por adelantado porque se entrega en dos días. No incluye arreglar
nada: eso se cotiza aparte y ya sabrás exactamente qué estás arreglando. Y si
sale mejor hacerla de nuevo, te lo digo igual.
Escríbeme por WhatsApp y te digo si vale la pena o si no me necesitas.
Los fondos de estas imágenes están generados con inteligencia artificial.

BOTÓN                 Enviar mensaje
MENSAJE PRECARGADO    Hola PanaClaw, quiero el Diagnóstico de Ventas

════════ ANUNCIO 08 · imagen única 9:16 · 1080×1920 ════════
Público: el que no tiene sitio · Producto: PanaClaw Start
Hipótesis: le duele que la dirección en internet no sea suya

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

════════ ANUNCIO 09 · imagen única 9:16 · 1080×1920 ════════
Público: el que tiene un WordPress que le da vergüenza · Producto: Diagnóstico
de Ventas
Hipótesis: le duele llevar meses sin saber qué pasó

FONDO
Tres bloques de cristal rojo encajándose uno dentro de otro, vistos desde
arriba y de cerca. El tercero todavía no ha terminado de entrar y la junta
abierta deja escapar luz. [BLOQUE DE ESTILO] [ENCUADRE 9:16] [NEGATIVOS]

ANTETÍTULO   DIAGNÓSTICO DE VENTAS
TITULAR      Antonio 700, 132 px, tres líneas, centro óptico y=880
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

════════ ANUNCIO 10 · imagen única 4:5 · 1080×1350 ════════
Público: el que invierte en publicidad · Producto: Diagnóstico de Ventas
Hipótesis: le duele pagar clics que caen en una página lenta

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

════════ ANUNCIO 11 · imagen única 9:16 · 1080×1920 ════════
Público: el que invierte en publicidad · Producto: Diagnóstico de Ventas
Hipótesis: le duele que nadie le dé una cifra por la página, sabiendo lo que le
cuesta un clic

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

════════ ANUNCIO 12 · imagen única 4:5 · 1080×1350 ════════
Público: el que invierte en publicidad · Producto: Diagnóstico de Ventas
Hipótesis: le duele llevar meses gastando sin saber si la página tiene arreglo

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
9. ANTES DE DEVOLVER, COMPRUEBA
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

No escribiste, redactaste, completaste, acortaste, tradujiste ni "mejoraste"
ningún texto. Todo lo que aparece en el documento, la ficha de campaña
incluida, está copiado carácter por carácter de lo que te di, con sus tildes,
sus eñes y sus puntos finales.

  [ ] ¿Está la ficha de campaña completa en el panel del principio, literal?
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
  [ ] ¿El orden del bloque es antetítulo, titular, cifra, nota, en las 16?
  [ ] ¿Las tres tarjetas de cada carrusel están ancladas en y=594, sin saltar?
  [ ] ¿El símbolo y el wordmark están en las tres tarjetas de cada carrusel?
  [ ] ¿Hay alguna caja, franja, tarjeta o sombra detrás de algún texto?
  [ ] ¿El wordmark dice PANACLAW en #FFF7F7 con el punto final en #FF5100?
  [ ] ¿El símbolo lleva fill-rule="evenodd" y conserva su proporción
      100 × 81.56, sin estirar?
  [ ] ¿Las doce piezas 4:5 exportan a 1080×1350 exactos y las cuatro 9:16 a
      1080×1920 exactos?
  [ ] ¿Están las cinco trampas del exportador resueltas, en particular el
      reinicio de ctx.letterSpacing a '0px' y ctx.textBaseline='top'?
````

---

## PARTE 4 · Qué comprobar cuando devuelva el documento

1. **Descarga una pieza y ponla al lado de su vista previa.** Si no son
   idénticas, el exportador está mal, y si está mal en una está mal en las
   dieciséis. Un desfase de dos o tres píxeles es normal; por encima de seis,
   algo está mal calculado.
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
6. **Desliza los dos carruseles.** Si el bloque de texto salta de sitio entre
   tarjetas, el anclaje no se respetó y se ve inmediatamente.

---

## PARTE 5 · Qué hacer con el orgánico que ya está programado

Las dos semanas a las 8:00 y a las 11:00 no se tocan, y la pauta tampoco las
necesita. Cuatro cosas que sí importan:

1. **No promociones ninguna publicación.** Ya está dicho en la Parte 1: crea una
   campaña paralela que compite por el mismo público con el mismo dinero.
2. **Los doce creativos de pauta son distintos de los orgánicos.** Si se repite
   una pieza en los dos sitios, el motor de entrega la agrupa con la orgánica y
   las hace competir entre sí en vez de ampliar el alcance.
3. **El perfil ya se ve habitado**, y eso importa más de lo que parece: alguien
   que ve un anuncio en frío y toca el nombre de la cuenta llega a un perfil con
   contenido, no a uno vacío. Ese era el argumento más fuerte para esperar antes
   de arrancar pauta y ya está resuelto.
4. **A las dos semanas hay público de interacción** de Instagram y Facebook.
   Todavía no da para un conjunto propio con este presupuesto, y forzarlo
   partiría la señal del único conjunto que hay. Cuando Meta deje de marcarlo
   como demasiado pequeño, **es una campaña aparte, no un segundo conjunto
   dentro de esta.**

---

## PARTE 6 · Qué NO incluye este entregable

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
- **No hay campaña de remarketing todavía**, ni de sitio ni de interacción. Los
  públicos y qué anunciarle a cada uno están en `campanas/canales/meta.md`, para
  cuando haya volumen.
- **No hay campaña de Google.** Se puede correr pero no leer: falta configurar
  Google Analytics 4.
- **El sitio no recibe pauta en esta fase.** El porqué está entero en la Parte 1.

---

## PARTE 7 · Decisiones que el dueño de la marca podría querer distintas

1. **Los creativos llevan el texto compuesto dentro de la imagen.**
   `campanas/plantillas/estructura-anuncio.md` pone «texto en imagen» por
   defecto en «no». Aquí va en «sí»: en frío y compitiendo con todo el feed, el
   titular dentro de la pieza es lo que detiene el pulgar, y el sistema visual de
   la marca está construido exactamente para sostener un titular. El copy
   completo va igualmente en los campos del editor de anuncios.
2. **La retícula de 1080×1920 está derivada, no copiada.** `datos/marca.json`
   declara el lienzo de story y dice que los márgenes laterales no cambian y que
   los anclajes verticales se recalculan, pero **no publica los valores
   recalculados**. Los de este entregable —símbolo en y=312, centro óptico en
   y=880, wordmark con base en y=1500— son un cálculo hecho aquí contra las
   zonas seguras del 15 % y el 20 %. Si se aprueban, su sitio es
   `datos/marca.json` → `redesSociales.reticula`, no este archivo.
3. **Dos de los doce anuncios son carrusel.** No estaban en la primera versión.
   Entran porque el formato es uno de los cuatro ejes de variación que el canal
   reconoce, y porque los dos conceptos que llevan —qué entra y qué no en Start,
   y el entregable del Diagnóstico— tienen tres tiempos naturales. Cuestan seis
   fondos en vez de dos.
4. **El presupuesto está por debajo del rango documentado.** $15 al día <!-- v: presupuesto diario del cliente, no un precio del catálogo -->
   funciona, pero tarda: el mismo gasto que produce datos legibles en 5–7 días a
   $20–50 diarios tarda de 7 a 10 a este ritmo. La alternativa no es repartirlo <!-- v: rango de presupuesto diario de campanas/canales/meta.md, no un precio del catálogo -->
   mejor entre más conjuntos, es esperar más antes de leer nada.
