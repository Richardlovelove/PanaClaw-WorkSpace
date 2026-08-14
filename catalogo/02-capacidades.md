# 02 · Capacidades avanzadas

Cosas que se suman a cualquier plan web. Pago único, por capacidad.

**Cifras:** [`datos/precios.json` → `capacidades`](../datos/precios.json)

> **Se llaman «capacidades avanzadas», nunca «módulos»** de cara al cliente.
> «Módulo» es una palabra de programador y no dice qué se consigue.

---

## Las seis

Cada una se describe por **lo que consigue el cliente**, nunca por con qué se
construye. Estas descripciones son las oficiales; úsalas tal cual.

| Capacidad | Precio | Qué consigue |
|---|---|---|
| Conexión con otro sistema | $350 | Tu web y el programa que ya usas dejan de vivir por separado |
| Cuentas de usuario | $450 | Cada persona entra con su clave y ve solo lo que le corresponde |
| Control de inventario | $550 | El stock se descuenta solo y dejas de vender lo que no tienes |
| Reservas y citas | $600 | Tus clientes reservan solos, sin llamarte y sin pisarse el horario |
| Panel de control | $650 | Ves tus números y gestionas tu negocio desde una sola pantalla |
| Portal de clientes | $750 | Cada cliente entra y consulta lo suyo sin escribirte para preguntar |

---

## Por qué las descripciones son así

Antes decían con qué se construye —«Supabase Auth + RLS»—. Eso le importa a un
programador; a quien va a pagar le dice cero y le hace sentir que no entiende lo
que compra.

Es la regla madre de la voz de la marca aplicada al catálogo técnico: **el dolor
antes que la herramienta**. Si te piden describir una capacidad nueva, la
descripción se escribe en esta forma o no se escribe.

---

## Con qué plan se combinan

Las capacidades **se suman a un plan**, no lo sustituyen. En el cotizador del
sitio, pedir una capacidad avanzada eleva automáticamente el plan mínimo
necesario:

- Reservas, portal de clientes o panel interno → mínimo **Corporate**
- Catálogo con cobro → **Commerce**

Un anuncio que ofrezca «reservas en línea desde $600» sin decir que hace falta un
plan debajo está anunciando un precio imposible. La forma correcta:
**«Corporate $850 + reservas $600»**, con los dos números.

---

## Qué NO es una capacidad avanzada

**Respuestas automáticas con IA.** Existió como capacidad ($250–$900) y se retiró <!-- v: precio histórico de un producto retirado -->
al publicarse eBot.

El motivo está documentado en el repositorio del sitio y conviene entenderlo,
porque explica cómo razona la marca: su descripción era literalmente lo que hace
eBot. Con los dos publicados, el sitio ofrecía **dos precios distintos para lo
que el cliente lee como una sola cosa**, y uno de ellos era un rango de casi
setecientos dólares de ancho. Eso desmonta la promesa de precios claros sobre la
que se sostiene el resto.

> Si alguien pide «IA dentro del sistema del cliente», eso es otro producto y
> necesita otro nombre y otro precio. Hoy **no existe**. No lo inventes: ofrece
> eBot ([03](03-ebot.md)) o di que no está en el catálogo.
