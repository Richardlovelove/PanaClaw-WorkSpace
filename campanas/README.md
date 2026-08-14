# Campañas

La arquitectura del embudo. **No hay campañas guardadas aquí** — hay la
estructura con la que se arma cualquiera.

---

## El embudo, en tres etapas

```
FRÍO          No conoce la marca. Le duele algo y no sabe que tiene arreglo.
  ↓           Objetivo: que reconozca su situación y vea una cifra.
TIBIO         Visitó el sitio y no escribió. Vio el precio.
  ↓           Objetivo: quitar la objeción concreta que lo frenó.
DECISIÓN      Llegó al cotizador o al formulario y no envió.
              Objetivo: una promesa de propiedad o de límite. Nada más.
```

**La marca no tiene etapa de «fidelización» todavía.** Con el sitio en beta y sin
clientes captados por campaña, inventar esa etapa sería producir piezas para un
público que no existe.

---

## Qué se dice en cada etapa

| Etapa | Qué se dice | Qué NO se dice |
|---|---|---|
| **Frío** | La situación del público + la cifra | Objeciones — todavía no tiene ninguna |
| **Tibio** | La objeción principal de ese público, contestada entera | El precio otra vez: ya lo vio |
| **Decisión** | Una sola promesa: el código es tuyo / los cambios tienen número | Urgencia, descuentos, cuenta atrás |

La lista de objeciones por público está en
[`adn/04-audiencia.md`](../adn/04-audiencia.md).

---

## Producto de entrada por etapa

No todos los productos sirven para entrar en frío. Solo dos tienen una cifra lo
bastante baja como para decidirse dentro de un anuncio:

| Etapa | Producto | Por qué |
|---|---|---|
| Frío | **Diagnóstico de Ventas $49** | La cifra más baja del catálogo. Produce una conversación con datos en la mano |
| Frío | **Start $295** | La cifra que abre la categoría |
| Tibio | Corporate $850 · eBot $499 | Ya conoce la marca; aquí es donde está el margen |
| Tibio | Auditoría $80–$150 | Público distinto: el que ya tiene sitio |
| Decisión | El que estuviera cotizando | — |

**Commerce ($1,200) y Care no se anuncian en frío.** El primero necesita un
recorrido; el segundo solo le sirve a quien ya es cliente.

---

## Las cuatro campañas base

Cuatro arquitecturas. Cualquier petición real es una de estas o una combinación.

### 1 · Captación por precio

**Para:** el que no tiene sitio o tiene uno que le da vergüenza.
**Ángulo:** la cifra publicada. Es lo que nadie más da.
**Entrada:** Start $295 o Diagnóstico $49.
**Destino:** `/planes/` en frío, `/cotizador/` en tibio.
**Se mide:** clics al cotizador y envíos del formulario.

### 2 · Captación por propiedad

**Para:** el que ya pasó por una agencia.
**Ángulo:** el código y el dominio quedan a su nombre.
**Entrada:** Corporate $850.
**Destino:** `/proceso/`, que es donde está el argumento entero.
**Se mide:** tiempo en `/proceso/` y clics a WhatsApp.

> Es la campaña con el argumento más fuerte y el público más pequeño. Rinde mejor
> en tibio y en remarketing que en frío.

### 3 · eBot

**Para:** el que no da abasto con los mensajes. Público distinto de los tres de
arriba: puede no necesitar web.
**Ángulo:** pago único, sin mensualidad. **Con los dos costos de terceros
publicados en la misma pieza.**
**Destino:** `/ebot/`.
**Se mide:** envíos del formulario con eBot elegido.

### 4 · Seguridad

**Para:** el que ya tiene sitio, casi siempre WordPress.
**Ángulo:** el procedimiento, **nunca el miedo**. Es el público más escéptico del
catálogo.
**Entrada:** Auditoría $80–$150.
**Destino:** `/seguridad/`.
**Se mide:** envíos con un plan de seguridad elegido.

---

## Cómo se arma una campaña

Cinco pasos. En este orden, y el orden importa: producir piezas antes de aprobar
la estructura es el desperdicio más caro.

1. **Público y momento.** Uno de los seis de
   [`adn/04-audiencia.md`](../adn/04-audiencia.md). Uno, no tres.
2. **Producto y precio.** Verificado contra
   [`datos/precios.json`](../datos/precios.json).
3. **Ángulo.** Precio, propiedad, plazo o velocidad. **Uno solo por campaña.**
4. **Piezas por etapa**, con su destino y su métrica.
5. **Producir.** Copy con
   [`prompts/texto/anuncios.md`](../prompts/texto/anuncios.md), visual con
   [`prompts/imagen/`](../prompts/imagen/).

**Los pasos 1–4 se entregan y se aprueban antes del 5.**

---

## Qué se mide

Solo lo que el sitio puede medir hoy. Está en
[`datos/marca.json`](../datos/marca.json) → `medicion`:

- **Píxel de Meta activo** (`1067898639025746`)
- **Evento `Lead`**, que se dispara **solo en `/gracias/`** — el único punto del
  sitio donde alguien ha completado algo
- **Google Analytics 4: sin configurar.** Falta el identificador de medición

**Consecuencia práctica:** hoy el recorrido solo se ve en Meta. Una campaña de
Google Ads no se va a poder medir bien hasta que se configure GA4. Está anotado
en [`operacion/deuda-conocida.md`](../operacion/deuda-conocida.md).

**No propongas métricas que no se pueden medir.** Nada de «tasa de conversión por
canal» ni «coste por cliente» mientras solo haya un píxel y un evento.

---

## Dos avisos antes de arrancar pauta


### 1 · No hay dominio propio

El sitio vive en `panaclaw.netlify.app`. Un anuncio pagado que lleva a un
subdominio de Netlify contradice el pilar de «el sitio es tuyo» en el primer
clic, y es lo primero que va a notar alguien que esté evaluando agencias.

### 2 · Google no se puede medir todavía

Falta configurar Google Analytics, así que una campaña de Google se puede correr
pero no leer. Meta sí tiene medición.

Las dos cosas están en
[`operacion/deuda-conocida.md`](../operacion/deuda-conocida.md). Dilo antes de
producir, no después.

---

## Plantillas

- [`plantillas/estructura-anuncio.md`](plantillas/estructura-anuncio.md) — una
  pieza de pauta, campo a campo
- [`plantillas/calendario.md`](plantillas/calendario.md) — cómo se reparte el mes
- [`canales/meta.md`](canales/meta.md) · [`canales/google.md`](canales/google.md)
  · [`canales/whatsapp.md`](canales/whatsapp.md)
