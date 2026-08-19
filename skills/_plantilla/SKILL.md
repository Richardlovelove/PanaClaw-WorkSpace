# Skill · [nombre]

Una línea: qué produce esta skill.

---

## 1 · Cuándo se usa

**Se dispara con:**
- «[frase literal que diría el humano]»
- «[otra frase]»

**NO se usa cuando:**
- [caso que parece este pero va a otra skill] → usa [`otra-skill`](../otra-skill/SKILL.md)

---

## 2 · Qué se lee

En este orden:

1. [`archivo`](../../ruta/archivo.md) — qué aporta
2. [`archivo`](../../ruta/archivo.md) — qué aporta

Y siempre, si el entregable es de cara al cliente:
[`adn/02-voz-y-tono.md`](../../adn/02-voz-y-tono.md). Y si la skill produce
texto de cara al cliente, también [`adn/06-claridad.md`](../../adn/06-claridad.md)
y [`adn/07-redaccion.md`](../../adn/07-redaccion.md).

---

## 3 · Qué se pregunta antes de empezar

Los datos sin los que el trabajo se hace dos veces:

1. **[Dato]** — por qué cambia el resultado
2. **[Dato]** — por qué cambia el resultado

Si el humano ya los dio, no preguntes nada y produce.

**Valores por defecto**, si el humano dice «lo que veas»:
- [dato] → [valor]

---

## 4 · Procedimiento

### Paso 1 · [nombre]

Qué se hace.

### Paso 2 · [nombre]

Qué se hace.

### Paso 3 · Entregar

Con qué forma sale. Ver
[`orquestador/protocolo-entrega.md`](../../orquestador/protocolo-entrega.md).

---

## 5 · Verificación

Antes de entregar, una a una:

- [ ] ¿Toda cifra existe en [`datos/precios.json`](../../datos/precios.json)?
- [ ] ¿Todo hex sale de [`datos/marca.json`](../../datos/marca.json)?
- [ ] ¿Algún pago único sumado a una mensualidad?
- [ ] ¿Jerga? (`Jamstack`, `CDN`, `stack`, `deploy`, `framework`, `headless`)
- [ ] ¿Algún dato, métrica o testimonio que no exista?
- [ ] ¿Huecos sin resolver — `[completa aquí]`, corchetes vacíos?
- [ ] ¿Se dice qué NO incluye?
- [ ] [comprobación específica de esta skill]

---

## Qué se dice al entregar

Tres cosas como máximo:
1. Qué es y para qué formato
2. **Qué no incluye o qué quedó pendiente**
3. Solo si aplica: qué decisión tomaste que el humano podría querer distinta
