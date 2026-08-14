# Plataforma · Pomelli (Google Labs)

Pomelli es la herramienta de marketing con IA de Google Labs y DeepMind. Funciona
en tres pasos: **analiza el sitio web en vivo** para construir un perfil de
«Business DNA» —tono de voz, paleta, tipografías, estilo visual—, propone ideas
de campaña y genera piezas de marca.

No se le pega un prompt: **se le da una URL y después se corrige lo que dedujo
mal.** Este archivo es sobre lo segundo.

---

## ⚠️ Advertencia crítica — leer antes de conectarlo

> **Hoy, Pomelli va a deducir el nombre de marca equivocado.**

La imagen social del sitio (`public/og.png`, la que se ve al compartir cualquier
enlace) lleva el wordmark **«CuatroNodos»**, un nombre de marca anterior. Está
generada por `scripts/generate-brand-assets.mjs`, que todavía tiene ese texto
escrito dentro.

Ese archivo es exactamente el tipo de recurso que una herramienta de análisis de
marca prioriza: es la imagen que el sitio se declara a sí mismo como
representativa.

**Además**, el mismo `og.png` lleva la frase «Sitios Jamstack en Panamá», que
infringe la regla de cero jerga. Si Pomelli la absorbe, va a producir copy con
esa palabra dentro.

### Qué hacer

**Antes de conectar Pomelli**, arreglar el origen: cambiar `CuatroNodos` por
`PanaClaw` y la bajada por una sin jerga en
`scripts/generate-brand-assets.mjs`, correr `npm run brand` y commitear el
`og.png` regenerado.

Está anotado en
[`operacion/deuda-conocida.md`](../../operacion/deuda-conocida.md) como el punto
que **bloquea** este flujo de trabajo.

**Si no se puede arreglar antes**, hay que revisar a mano el DNA que produzca
Pomelli y corregir el nombre y la descripción, en cada campaña, cada vez.

---

## Qué darle

**URL:** `https://panaclaw.netlify.app`

> Hoy el sitio está en beta, publicado sin dominio propio. Cuando haya dominio,
> se le da el dominio: es lo que va a quedar guardado en el perfil.

---

## Qué corregir después del análisis automático

Pomelli deduce; no acierta todo. Repasa estos campos contra
[`datos/marca.json`](../../datos/marca.json) y
[`adn/`](../../adn/), y corrige.

### Nombre y descripción

| Campo | Valor correcto |
|---|---|
| Nombre | `PanaClaw` |
| Tagline | `Sitios rápidos. Código tuyo.` |
| Descripción | `Agencia web en Panamá. Sitios que abren en menos de un segundo, entregados en días y que quedan a tu nombre. Desde $295.` |
| Mercado | Panamá |
| Idioma | Español (es-PA) |

**Comprueba el nombre aunque no esperes un error.** Es el campo que la advertencia
de arriba compromete.

### Paleta

Lo que la herramienta extraiga del CSS debería estar cerca, pero suele añadir
colores intermedios que no son tokens de marca. Déjala en exactamente cinco:

```
#100101   fondo
#FF5100   acento único
#FF1E1E   solo fondos
#FFF7F7   texto
#BABABA   texto secundario
```

**Y comprueba que no haya colado ningún azul.** Es el error más frecuente de
cualquier extractor automático sobre un sitio oscuro.

### Tipografía

**Archivo**, una sola familia, pesos 300–700. Si propone una segunda fuente para
titulares o para cuerpo, quítala.

### Tono de voz

Casi seguro que va a deducir algo genérico —«profesional y cercano»—. Sustitúyelo
por el bloque de [`prompts/bloques/voz.md`](../bloques/voz.md). Usa la **versión
corta** si el campo tiene límite, la larga si no.

### Estilo visual

Si el campo lo permite, describe la estética con el bloque de
[`prompts/bloques/estilo-visual.md`](../bloques/estilo-visual.md) y añade lo
prohibido: sin personas, sin oficinas, sin azul, sin fondos claros.

---

## Antes de generar campañas

Pomelli propone ideas de campaña a partir del DNA. Antes de aceptar ninguna,
dale el contexto que **no puede deducir del sitio**:

### 1 · Los precios, literales

Copia de [`datos/precios.json`](../../datos/precios.json) los que vayas a usar,
con esta instrucción:

```
Estas cifras son exactas y no se pueden cambiar, redondear ni estimar. Un
importe de pago único y uno mensual no se suman nunca: se presentan como dos
totales separados.
```

### 2 · Lo que no existe

```
No hay testimonios de clientes, ni número de clientes, ni años de experiencia,
ni métricas de resultado, ni logos de clientes, ni premios. No los inventes ni
los uses como marcador de posición.
```

Es la instrucción más importante que le puedes dar a una herramienta de
generación de campañas, porque el testimonio inventado es su salida por defecto.

### 3 · Lo prohibido

```
No prometas posicionamiento en Google. No uses urgencia ni descuentos: no
existen. Sin emojis ni signos de exclamación.
```

---

## Revisión de lo que produzca

Todo lo que salga de Pomelli pasa por
[`orquestador/protocolo-entrega.md`](../../orquestador/protocolo-entrega.md)
igual que si lo hubieras escrito tú. Lo que más falla:

- [ ] ¿Dice `PanaClaw` en todas partes? → busca «CuatroNodos»
- [ ] ¿Aparece «Jamstack» o cualquier otra jerga?
- [ ] ¿Se coló azul en alguna pieza?
- [ ] ¿Hay personas en las imágenes?
- [ ] ¿Inventó un testimonio, una métrica o un número de clientes?
- [ ] ¿Las cifras coinciden con `precios.json`?
- [ ] ¿Sumó un pago único con una mensualidad?
- [ ] ¿Emojis o exclamaciones?

---

## Lo que Pomelli hace bien y lo que no

**Bien:** producir volumen de piezas coherentes en paleta y tipografía, adaptar
un formato a varios canales, proponer ángulos de campaña que no se te habían
ocurrido.

**Mal, con esta marca en concreto:** el copy. La voz de PanaClaw se define por
cosas que un generador de marketing hace exactamente al revés —decir qué no
incluye, desaconsejar una compra, no usar urgencia, dar la cifra sin adornar—.

**Recomendación:** usa Pomelli para el **volumen visual** y escribe el copy
contra este repositorio. Sustituir el texto de una pieza es rápido; corregir una
voz equivocada en 40 piezas, no.

---

**Fuentes sobre el funcionamiento de Pomelli:**
[Google Blog](https://blog.google/innovation-and-ai/models-and-research/google-labs/pomelli/) ·
[Search Engine Journal](https://www.searchenginejournal.com/google-labs-deepmind-launch-pomelli-ai-marketing-tool/559569/)
