# Canal · Google Ads

---

## ⚠️ Antes de arrancar: falta la medición

**Google Analytics 4 no está configurado.** El identificador (`G-…`) está vacío
en el sitio, a propósito, para no dejar un placeholder falso midiendo en la
cuenta de nadie.

Sin GA4:

- No se puede importar la conversión a Google Ads
- No se puede optimizar por conversiones — solo por clics
- No se ve el recorrido del que entra por Google

**Consecuencia:** una campaña de Google hoy se puede correr, pero **no se puede
leer**. Está anotado en
[`operacion/deuda-conocida.md`](../../operacion/deuda-conocida.md).

Meta ([`meta.md`](meta.md)) sí tiene medición y es donde debería ir el
presupuesto mientras esto no se resuelva.

---

## Por qué Google encaja bien con esta marca

Cuando la medición esté lista, Google es el canal más natural del catálogo, y por
una razón concreta: **quien busca «cuánto cuesta una página web en Panamá» está
buscando literalmente lo único que esta marca publica y la competencia no.**

En Meta hay que interrumpir a alguien y convencerlo de que tiene un problema. En
Google ya lo sabe y está preguntando el precio.

---

## Búsqueda — grupos de anuncios

Cuatro grupos, uno por intención. Nada de un grupo genérico de «diseño web».

| Grupo | Intención | Destino |
|---|---|---|
| Precio | «cuánto cuesta una página web panamá», «precio diseño web panamá» | `/planes/` |
| Tienda | «hacer tienda en línea panamá», «vender en línea yappy» | `/planes/` |
| Bot | «bot whatsapp negocio», «responder mensajes automático» | `/ebot/` |
| Seguridad | «seguridad wordpress», «me hackearon la página» | `/seguridad/` |

**El grupo «Precio» es el importante.** Es donde la marca gana sin competir: el
anuncio puede llevar la cifra y ninguno de los demás la lleva.

---

## Límites de texto

| Campo | Límite | Cuántos |
|---|---|---|
| Título | 30 caracteres | 3–15 |
| Descripción | 90 caracteres | 2–4 |

Con 30 caracteres, un título es una cosa y solo una:

```
$295. Web lista en 72 horas.     (28)
El código queda a tu nombre       (28)
Precio publicado, sin sorpresas   (31 — no cabe, hay que recortar)
```

**Cuenta los caracteres.** Un título que se corta a mitad de la cifra es peor que
no ponerla.

---

## Negativas obligatorias

Sin estas, el presupuesto se va en tráfico que nunca va a comprar:

```
gratis · gratuito · curso · cursos · tutorial · aprender · cómo hacer ·
plantilla · plantillas · wordpress gratis · wix · plantilla html ·
empleo · trabajo · vacante · salario · freelance · portafolio
```

**`gratis` es la primera y la más cara.** «Cómo hacer una página web gratis» es
una de las búsquedas más frecuentes de la categoría y no tiene nada que ver con
este negocio.

---

## Display

Formato 1.91:1 (1200 × 628), texto en la mitad izquierda. Ver
[`prompts/bloques/encuadre.md`](../../prompts/bloques/encuadre.md).

**Display es para remarketing, no para frío.** En frío, el sistema visual de la
marca —negro casi puro— desaparece dentro de una página cualquiera. En
remarketing funciona bien: quien ya vio el sitio lo reconoce por el color.

---

## Lo que Google va a empujar y hay que rechazar

| Google sugiere | Por qué no |
|---|---|
| Recursos generados automáticamente | Escribe relleno de agencia y mete exclamaciones |
| Ampliación automática de palabras clave | Trae búsquedas de «gratis» y de empleo |
| Máximo rendimiento (Performance Max) | Genera creativo propio y no respeta el sistema visual |
| Anuncios adaptables con títulos automáticos | Combina títulos que contradicen la cifra |

**Desactiva los recursos generados automáticamente.** Es la opción que más rápido
rompe la voz.

---

## Antes de arrancar

- [ ] ¿GA4 configurado y la conversión importada? → **si no, no arranques**
- [ ] ¿Están las negativas, con `gratis` la primera?
- [ ] ¿Los títulos caben en 30 caracteres, contados?
- [ ] ¿Cada grupo tiene su destino propio?
- [ ] ¿Recursos automáticos desactivados?
- [ ] ¿Las cifras coinciden con `datos/precios.json`?
