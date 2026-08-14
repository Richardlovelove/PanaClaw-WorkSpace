# PanaClaw Workspace — Orquestador

Este repositorio es **el cerebro de la marca PanaClaw**, no un proyecto de
software. No se compila, no se despliega y no tiene interfaz. Existe para que
cualquier agente de IA —Claude, Grok, Gemini, Pomelli, el que sea— pueda entrar,
entender la marca en una sola lectura y devolver un entregable que suene, se vea
y cobre exactamente como PanaClaw.

**Si eres un agente y solo vas a leer un archivo, lee este.** Al final hay una
tabla que te manda al resto según lo que te haya pedido el humano.

---

## 1. Qué es PanaClaw en cuatro líneas

Agencia de sitios web en Panamá. Vende webs que abren en menos de un segundo,
se entregan en días en vez de meses, y cuyo código queda a nombre del cliente.
Desde $295. Además vende un bot multicanal (eBot), ciberseguridad web,
mantenimiento (Care) y un diagnóstico de ventas.

El argumento entero de la marca es **la ausencia de trampa**: precio publicado,
plazo publicado, lista de lo que NO está incluido publicada, y el código en manos
del cliente al terminar de pagar. Todo lo que produzcas tiene que sostener eso.

---

## 2. Las cinco reglas que no puedes romper

Estas cinco cuestan clientes si se rompen. La lista completa, con el porqué de
cada una, está en [`orquestador/reglas.md`](orquestador/reglas.md).

1. **Ninguna cifra que no esté en [`datos/precios.json`](datos/precios.json).**
   No inventes, no redondees, no proyectes, no estimes. Si te falta un precio, el
   producto no existe todavía y lo dices.
2. **Un importe de pago único y uno mensual NUNCA se suman.** Dos totales
   separados, siempre. Sumarlos da un número creíble y falso.
3. **Cero jerga.** Nada de Jamstack, CDN, LCP, headless, stack, deploy, SSG,
   Lighthouse ni «scope creep». Solo los nombres que un dueño de negocio panameño
   ya reconoce: WordPress, Google, WhatsApp, Instagram, Yappy, GitHub.
4. **Nada de datos inventados.** Métricas, testimonios, casos y logos de clientes
   solo si están verificados y con fecha. Una cifra inflada desmonta el argumento
   de las otras diez piezas.
5. **Un solo acento cromático: naranja `#FF5100`.** El rojo `#FF1E1E` es
   exclusivo de fondos y jamás toca un texto. Nada de azul, nunca.

---

## 3. Cómo está organizado este repositorio

```
datos/          Las dos fuentes de verdad. Máquina antes que prosa.
  precios.json    Toda cifra que la marca puede decir en voz alta
  marca.json      Todo token visual: hex, fuentes, formas, movimiento

adn/            Quién es la marca. Se lee antes de escribir una sola palabra.
catalogo/       Qué vende, en prosa. Capa legible sobre precios.json.
prompts/        ESTRUCTURAS de prompt por medio y por plataforma. No guiones.
campanas/       Arquitectura de campaña, embudo y plantillas de pieza.
skills/         Procedimientos empaquetados para agentes.
orquestador/    Reglas duras, enrutador y protocolo de entrega.
herramientas/   verificar.mjs — comprueba que nada de esto se haya desincronizado.
operacion/      Cómo se mantiene vivo este repositorio.
```

**La jerarquía de autoridad, cuando dos archivos se contradigan:**

```
datos/*.json  →  adn/*  →  catalogo/*  →  todo lo demás
```

Un `.md` que diga `$300` cuando `precios.json` dice `$295` está equivocado, y se <!-- v: contraejemplo, $300 es la cifra equivocada que se ilustra -->
corrige el `.md`. Nunca al revés.

---

## 4. Enrutador — qué leer según lo que te pidan

Lee siempre **`adn/02-voz-y-tono.md`** antes de escribir texto de cara al
cliente, y **`datos/marca.json`** antes de describir cualquier cosa visual. Eso
es la base. Encima de esa base, según la petición:

| Si el humano pide… | Lee, en este orden |
|---|---|
| Prompts de imagen, creativos, Nano Banana | `datos/marca.json` → `prompts/README.md` → `prompts/bloques/` → `prompts/imagen/nano-banana.md` |
| Imágenes **por lote** (10, 50, 200 piezas) | lo anterior + `prompts/imagen/lote.md` + `skills/lote-visual/SKILL.md` |
| Guion o prompt de video, reel, anuncio en video | `prompts/video/video-corto.md` + `adn/02-voz-y-tono.md` |
| Anuncios pagados (Meta, Google) | `campanas/plantillas/estructura-anuncio.md` + `campanas/canales/` + `catalogo/` del producto |
| Una campaña completa | `campanas/README.md` (el embudo entero) y de ahí a las plantillas |
| Alimentar Pomelli / Google Labs | `prompts/plataformas/pomelli.md` — **tiene una advertencia crítica, no la saltes** |
| Prompts para Grok, GPT u otro modelo ajeno | `prompts/plataformas/grok.md` |
| Diseños en Canva | `prompts/plataformas/canva.md` |
| Precios, cotizar, armar una propuesta | `datos/precios.json` → `catalogo/` → `skills/propuesta-comercial/SKILL.md` |
| Explicar un producto, comparar planes | `catalogo/` del producto + `catalogo/08-fronteras.md` |
| Copy de web, correo, WhatsApp, orgánico | `adn/02-voz-y-tono.md` + `prompts/texto/organico.md` |
| Responder una objeción de un cliente | `adn/04-audiencia.md` (las objeciones están catalogadas ahí) |
| Crear una skill nueva | `skills/README.md` + `skills/_plantilla/SKILL.md` |
| Saber si el repo está al día | `operacion/sincronizacion.md` + `node herramientas/verificar.mjs` |

---

## 5. Cómo se entrega

Todo entregable pasa por [`orquestador/protocolo-entrega.md`](orquestador/protocolo-entrega.md)
antes de salir. El resumen:

- **Un prompt se entrega listo para pegar.** Sin `[completa aquí]`, sin <!-- v: contraejemplos de huecos sin resolver -->
  `<tu producto>`, sin corchetes vacíos. Si te falta un dato, lo pides antes de <!-- v: contraejemplos de huecos sin resolver -->
  generar, no lo dejas como hueco.
- **Todo importe citado se verifica contra `datos/precios.json`** en el momento
  de escribirlo. No de memoria.
- **Todo hex se copia de `datos/marca.json`.** No «naranja», no «#FF5500», <!-- v: contraejemplo de hex equivocado -->
  no de memoria: `#FF5100`.
- **Di qué no incluye.** Es la firma de la marca y aplica también a tu trabajo:
  si el entregable tiene un límite, se dice arriba y no en una nota al pie.

---

## 6. Relación con el repositorio del sitio

El sitio vive en **`Richardlovelove/PanaClaw`** (Astro estático en Netlify). Ese
repositorio es la fuente original de casi todo lo que hay aquí: los precios salen
de `src/data/*.ts` y los tokens de `src/styles/global.css`.

**Este repositorio es un espejo, no una copia paralela.** Cuando cambie un precio
en el sitio, cambia aquí. El mapeo archivo-a-archivo y el procedimiento están en
[`operacion/sincronizacion.md`](operacion/sincronizacion.md), y
`node herramientas/verificar.mjs` detecta las divergencias más caras sin pedir
permiso a nadie.

No edites el sitio desde aquí, ni edites esto para «arreglar» algo que en
realidad está mal en el sitio. Si encuentras una contradicción, la reportas.

---

## 7. Lo que este repositorio NO es

- **No es un almacén de guiones escritos.** No hay copys finales guardados
  esperando a ser reutilizados. Hay estructuras: el copy se genera cada vez,
  contra el ADN, para el contexto concreto que pida el humano.
- **No es un histórico.** Lo que deja de ser cierto se borra, no se archiva. El
  historial de git ya guarda lo viejo.
- **No es documentación del código del sitio.** Eso está en el otro repositorio,
  en `docs/`.
