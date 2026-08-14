# 04 · Seguridad web

Ciberseguridad para un sitio **que ya existe**. Casi siempre WordPress.

**Cifras:** [`datos/precios.json` → `seguridad`](../datos/precios.json)
**Lectura obligatoria junto a este archivo:** [08 · Fronteras](08-fronteras.md)

---

## Frase oficial

> Revisamos cómo está montado tu sitio y por dónde podrían entrar, te lo
> entregamos por escrito y lo cerramos. La auditoría cuesta desde $80 y se paga
> una vez; si además quieres que quede protegido mes a mes, desde $30 al mes.

Tagline: **«Que no te lo hackeen.»**

---

## El gancho

No es el precio. Es la historia de al lado:

> Un negocio monta su web, pasan unos meses y un día aparece caída, redirigiendo
> a una página de pastillas o pidiendo un rescate. Casi siempre es lo mismo: un
> complemento sin actualizar y una contraseña que nunca cambió.

---

## La regla que gobierna este producto

> **La Auditoría es obligatoria, se paga siempre y aparte, y no va incluida en
> ningún plan mensual.**

No es cosmético. Regalarla dentro del mensual significa revisar gratis a quien
luego no contrata, y **proteger sin haber revisado es proteger a ciegas**.

Orden de venta: auditoría primero, mensual después. Es lo contrario del anclaje
de los planes web (donde va primero el caro) porque aquí lo que hay que vencer no
es el precio: es que nadie se suscribe a proteger algo que todavía no sabe si
está roto.

---

## Auditoría de Seguridad · $80–$150 · informe en 5 días

Pago único. El informe es del cliente **aunque no contrate ningún plan después**.

**Los tres tramos** — así se identifica cuál toca, por cómo reconoce el cliente su
propio sitio y no por cuántas páginas cuenta:

| Tramo | Cómo lo reconoce el cliente | Precio |
|---|---|---|
| Chico | Una página o unas pocas secciones. Informativo | $80 | <!-- v: precio exacto del tramo, no el mínimo de un rango -->
| Medio | Varias páginas, blog o formularios. Gestor de contenidos con complementos | $110 |
| Tienda | Una tienda o un sistema con cuentas. Cobros, usuarios, años de complementos | $150 | <!-- v: precio exacto del tramo, no el mínimo de un rango -->

**Por qué es un rango, y se dice junto al precio:**

> No cuesta lo mismo revisar una página de cinco secciones que una tienda con
> cuentas, pagos y tres años de complementos encima. La cifra exacta va por
> escrito antes de empezar.

**Qué se mira:**
- Cómo está montado y dónde vive: alojamiento, dominio, certificados
- Si funciona como debe: cifrado, formularios, accesos, páginas de error
- Por dónde podrían entrar: los diez fallos por los que más se entra en una web
- Se deja la entrada con verificación en dos pasos y las contraseñas cambiadas
- Informe en español, con lo urgente arriba

---

## Los dos planes mensuales

Los dos **exigen la auditoría antes**. Se dice debajo del precio, no en la letra
pequeña.

### Web Protegida · $30–$60/mes · ★

La protección del día a día, una vez sabemos cómo está el sitio.

- Un filtro delante que bloquea los ataques antes de que lleguen
- Se cierran las puertas que el gestor de contenidos deja abiertas de fábrica
- Revisión completa **cada tres meses**, no solo el primer día
- Cada mes se mira quién tiene acceso y con qué permisos
- Aviso de cookies y datos personales **en regla con la ley panameña**
- Informe mensual

### Web Blindada · $70–$120/mes

Lo mismo, sin esperar a que pase algo.

- Todo lo de Web Protegida
- Revisión completa **cada mes** en vez de cada tres
- Vigilancia de si alguien cambia o mete algo en el sitio
- **Respuesta en 24–48 h si hay un incidente**, y entramos a contenerlo
- Informe de cada cambio de acceso

---

## Comparativa

| | Auditoría | Protegida | Blindada |
|---|---|---|---|
| Revisión completa | Una vez | Cada 3 meses | Cada mes |
| Cifrado y certificados | ✓ | ✓ | ✓ |
| Verificación en dos pasos | ✓ | ✓ | ✓ |
| Quién tiene acceso | Se deja en orden | Cada mes | Cada mes |
| Informe | Una vez | Mensual | Mensual |
| Filtro que bloquea ataques | — | ✓ | ✓ |
| Puertas del gestor cerradas | — | ✓ | ✓ |
| Cookies y datos en regla | — | ✓ | ✓ |
| Vigilancia de cambios | — | — | ✓ |
| Respuesta a incidente | — | — | 24–48 h |
| **Mantenimiento, copias y actualizaciones** | **Eso es Care** | **Eso es Care** | **Eso es Care** |

La última fila no compara nada: dice lo que **no está** en este producto. Es la
que más preguntas ahorra, porque el solape con Care es la confusión más cara del
catálogo. **Inclúyela siempre que reproduzcas esta tabla.**

---

## Cómo se hace — los cuatro pasos

Van publicados porque en seguridad la objeción no es el precio, es «¿y qué me vas
a hacer exactamente?». Un servicio que no cuenta su procedimiento se parece
demasiado a quien te llama para decirte que tu computadora tiene un virus.

1. **Nos das permiso, por escrito.** Nada se toca sin autorización y sin saber que
   el sitio es del cliente. Se firma qué se revisa y qué no.
2. **Miramos cómo está montado.** Dónde vive, con qué está hecho, quién tiene
   llaves.
3. **Buscamos por dónde se entra.** Con las mismas herramientas que usa quien
   ataca, pero sin romper nada: se prueba la puerta, no se tira abajo. Fuera de
   hora punta.
4. **Te lo contamos y lo cerramos.** Informe con lo urgente arriba, cada cosa
   explicada en lo que le puede pasar y no en su nombre técnico. Al terminar se
   vuelve a mirar: lo que se arregló tiene que salir arreglado.

---

## Qué NO incluye

En seguridad esto importa el doble: es el único servicio del catálogo donde
prometer de más no se paga con una discusión, sino con un cliente hackeado que
creía estar cubierto.

- **La promesa de que no te van a hackear nunca** — eso no lo puede firmar nadie,
  y quien lo firme te está mintiendo
- El mantenimiento del sitio: actualizaciones, copias y caídas son **Care**
- Recuperar un sitio **ya hackeado**: es otro trabajo y se cotiza aparte
- Rehacer el sitio si resulta que está mal construido de raíz
- Lo que cobren terceros si el caso pide un plan de pago en el filtro o el
  alojamiento
- Auditar lo que no sea el sitio web: redes internas, computadoras o correo

---

## Las dos objeciones clave

**«Mi sitio es pequeño, ¿quién va a querer atacarlo?»**
Nadie te eligió a ti. Los ataques que tumban sitios pequeños son automáticos: un
programa recorre internet probando la misma puerta en millones de webs y entra en
las que la tienen abierta. No mira si vendes mucho o poco, mira si el complemento
que usas tiene un fallo conocido. Por eso es tan barato protegerse y tan caro no
hacerlo.

**«Si el sitio me lo hicieron ustedes, ¿también lo necesito?»**
La mitad de esta lista no, y se le dice: lo que construye PanaClaw no lleva
complementos que actualizar ni panel público por el que entrar, que es por donde
se cuelan casi todos. Lo que sí suma en cualquier sitio: la auditoría de cómo
está montado, la verificación en dos pasos, el filtro delante y el aviso de
cookies.

> Esta segunda respuesta es la que mejor define a la marca: **desaconseja media
> venta**. No la suavices.

---

## Nota de origen

Los planes vienen del documento «Planes de Servicios: Web y Ciberseguridad». Tres
cosas cambiaron al publicarlos: los precios estaban en euros y aquí se cobra en
dólares (mismas cifras, que son números de venta y no una conversión contable);
la referencia al RGPD europeo pasa a **la ley panameña de datos personales**; y
el plan «Completo» del documento incluía mantenimiento web, que se sacó entero
porque eso es Care.
