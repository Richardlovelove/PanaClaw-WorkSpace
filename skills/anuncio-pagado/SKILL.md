# Skill · Anuncio pagado

Produce copy y especificación de piezas de pauta.

---

## 1 · Cuándo se usa

**Se dispara con:**
- «Anuncios para Meta / Instagram / Facebook»
- «Copy para pauta»
- «Necesito variantes para probar»
- «Una campaña de Google»

**NO se usa cuando:**
- Piden la campaña entera con su embudo → [`campanas/README.md`](../../campanas/README.md) primero
- Piden solo la imagen → [`lote-visual`](../lote-visual/SKILL.md)
- Piden contenido orgánico → [`prompts/texto/organico.md`](../../prompts/texto/organico.md)
- Piden una cotización para un cliente → [`propuesta-comercial`](../propuesta-comercial/SKILL.md)

---

## 2 · Qué se lee

1. [`adn/02-voz-y-tono.md`](../../adn/02-voz-y-tono.md)
2. [`adn/04-audiencia.md`](../../adn/04-audiencia.md) — los ganchos y las
   objeciones salen de aquí
3. [`datos/precios.json`](../../datos/precios.json) — **literal**, no de memoria
4. El [`catalogo/`](../../catalogo/) del producto que se anuncia
5. [`campanas/plantillas/estructura-anuncio.md`](../../campanas/plantillas/estructura-anuncio.md)
6. [`campanas/canales/`](../../campanas/canales/) — el del canal
7. [`prompts/texto/anuncios.md`](../../prompts/texto/anuncios.md)

---

## 3 · Qué se pregunta antes de empezar

1. **¿Qué producto?** Hay seis con seis precios y seis públicos.
2. **¿Etapa: frío, tibio o remarketing?** Cambia qué se dice por completo.
3. **¿A dónde cae el clic?** `/planes/`, `/cotizador/`, `/ebot/`, `/seguridad/`
   o WhatsApp.

**Por defecto**, si dicen «lo que veas»:
- Canal: Meta (es el único con medición activa)
- Etapa: frío
- Producto: Start $295 o Diagnóstico $49 — las dos cifras que funcionan en frío
- Destino: `/planes/`
- Cuatro variantes, una hipótesis cada una

---

## 4 · Procedimiento

### Paso 1 · Fijar público y ángulo

Un público de los seis. **Un solo ángulo**: precio, propiedad, plazo o velocidad.

### Paso 2 · Sacar el gancho

De la columna «situación» del público en
[`adn/04-audiencia.md`](../../adn/04-audiencia.md). Segunda persona, presente,
afirmativo. Sin nombrar la marca.

### Paso 3 · Verificar el precio

Abre [`datos/precios.json`](../../datos/precios.json) y **cópialo**. No de
memoria.

Comprueba: ¿es un rango? → entero o con «desde». ¿Hay una mensualidad de por
medio? → dos totales separados, nunca sumados.

### Paso 4 · Escribir las cuatro partes

`gancho → giro → cifra → límite`. Las cuatro.

El **límite** es el que hace que suene a esta marca: «el reloj arranca cuando nos
das tus textos y la mitad del pago», «los $5 de la nube se pagan aparte, no a
nosotros».

### Paso 5 · Comprobar los límites del canal

Meta: gancho y cifra dentro de los **primeros 125 caracteres**.
Google: títulos de **30 caracteres, contados**.

### Paso 6 · Variantes

Si piden varias, **una hipótesis por variante**. Todo lo demás igual: misma
imagen, mismo producto, mismo destino.

Cuatro redacciones del mismo mensaje no son cuatro variantes.

### Paso 7 · Entregar

Tabla: variante · hipótesis · gancho · cuerpo · CTA · destino.

---

## 5 · Verificación

- [ ] ¿Las cuatro partes, incluido el **límite**?
- [ ] ¿El gancho es una situación en 2ª persona y presente, sin nombrar la marca?
- [ ] ¿Cada cifra existe en `datos/precios.json`, verificada ahora?
- [ ] ¿Los rangos, enteros o con «desde»?
- [ ] ¿Algún pago único sumado a una mensualidad?
- [ ] ¿Si es eBot, están los dos costos de terceros?
- [ ] ¿Si es un mensual de seguridad, dice que la Auditoría va antes y aparte?
- [ ] ¿Emojis, exclamaciones, urgencia o descuentos inventados?
- [ ] ¿Se promete posicionamiento en Google?
- [ ] ¿Algún testimonio, métrica o número de clientes?
- [ ] ¿Una sola llamada a la acción?
- [ ] ¿El CTA de WhatsApp va sin número?
- [ ] ¿Cabe en el límite del canal, contado?
- [ ] ¿Cada variante prueba una hipótesis distinta?

---

## Qué se dice al entregar

1. Producto, público, etapa y canal
2. **Qué hipótesis prueba cada variante**
3. Si aplica: que Google no se puede medir todavía (falta GA4), o que el destino
   sigue siendo un subdominio de Netlify. Ver
   [`operacion/deuda-conocida.md`](../../operacion/deuda-conocida.md)
