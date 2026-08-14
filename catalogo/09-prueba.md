# 09 · Prueba

Lo único verificable que la marca puede decir hoy. Es menos de lo que a un
publicista le gustaría, **y ese es exactamente el punto**.

---

## La regla

> **Nada de datos inventados.** Métricas, testimonios y casos solo se publican
> medidos o verificados, y las cifras llevan la fecha de su medición. Un número
> sin fecha deja de ser cierto sin que nadie lo toque.

El motivo no es prudencia decorativa: el argumento entero de la marca es que los
números se miden. **Una cifra inflada aquí desmonta las otras diez piezas de la
campaña.**

Es preferible enseñar cuatro enlaces reales sin adornos que cuatro fichas
completas que no aguanten una comprobación.

---

## Lo que SÍ se puede decir

### Los cuatro proyectos publicados

Nombre, dominio, enlace y sector. **Nada más está verificado.**

| Proyecto | Dominio | Sector | Qué es |
|---|---|---|---|
| **StemFlow** | play.bukoflow.com | Música | Plataforma para escuchar música en tres dimensiones: cada instrumento se mueve por el espacio y se ajusta en tiempo real mientras suena |
| **LiveSync Pro** | livesyncpro.com | Software técnico | Suite de herramientas de cálculo para ingenieros: física, comportamiento térmico de equipos y gestión de inventario |
| **Acústica Superior** | acusticasuperior.com | Acústica | Sitio de una empresa panameña de tratamiento acústico, con camino directo a cotizar por WhatsApp |
| **Bukoflow Tienda** | tienda.bukoflow.com | Música | Tienda de beats con licencia inmediata: catálogo, compra en línea y producción a medida |

**Acústica Superior es el más útil en campaña local:** es el único cliente
panameño de la lista y el caso que mejor se parece al público objetivo.

### Las promesas verificables

Estas no necesitan un cliente que las respalde porque son comprobables por
cualquiera, el primer día:

- El sitio abre en menos de un segundo → se puede medir en vivo
- El código queda a nombre del cliente → está en el contrato
- El dominio queda a su nombre → se comprueba en el registro
- El precio está publicado → está en la web
- La lista de exclusiones está publicada → está en la web

**Cuando falte prueba social, usa una promesa verificable en su lugar.** «El
código queda a tu nombre» hace más trabajo que un testimonio inventado, y no se
cae.

---

## Lo que NO se puede decir

Nada de esto existe verificado hoy. **No lo produzcas, ni siquiera como
ejemplo o marcador de posición:**

- Testimonios de clientes
- Número de clientes, proyectos entregados o años de experiencia
- Métricas de rendimiento por proyecto (velocidad, puntuación de Google,
  conversión) — no están medidas
- Logos de clientes
- Premios, certificaciones o reconocimientos
- Comparativas de «antes y después» con cifras
- Porcentajes de mejora de cualquier tipo

> El único dato de mercado que el copy del sitio usa es que **cuatro de cada diez
> personas abandonan una página que tarda más de tres segundos**. Es una
> estadística de sector, no un resultado de PanaClaw, y así hay que presentarla
> si se usa.

---

## Cómo se completa una ficha de proyecto

Los cuatro proyectos están a medias a propósito. Para completar uno hacen falta
cuatro cosas, en este orden:

1. **Contenido** — sector, año, resumen, reto y solución. Los escribe quien hizo
   el proyecto. Mismo criterio que todo lo demás: el dolor del cliente antes que
   la herramienta.
2. **Métricas medidas** — `npm run medir` en el repositorio del sitio las mide y
   las devuelve con su fecha. **Si no se midió, el array queda vacío y la banda de
   métricas no aparece.** No se rellenan de memoria.
3. **Capacidades aplicadas** — con el vocabulario de
   [02 · Capacidades](02-capacidades.md), para que el visitante ate el caso con
   lo que puede contratar.
4. **Captura** — `npm run capturas` la genera. **Hay que mirarla antes de
   publicarla**: el script no distingue una portada de un aviso de cookies
   tapándola.

Una ficha a medias se ve corta pero nunca falsa. Es el intercambio correcto.

---

## Qué hacer cuando piden prueba social

| Piden | Se responde |
|---|---|
| Un testimonio | No hay testimonios verificados. Puedo usar los cuatro proyectos publicados con su enlace. |
| «X clientes satisfechos» | No hay una cifra verificada de clientes. |
| Métricas de un caso | No están medidas todavía. `npm run medir` las produce con fecha; hasta entonces no se publican. |
| Un caso de éxito con números | Puedo describir qué es cada proyecto, sin cifras de resultado. |
| Logos de clientes | Hay cuatro dominios públicos y enlazables. Logos, no. |

Ninguna de estas es una negativa a trabajar: es la marca funcionando. La promesa
de que no hay letra chica solo vale si también aplica hacia dentro.
