# Deuda conocida

Lo que hoy está mal o falta, y a qué trabajo bloquea.

**Regla de este documento:** lo que se cierra **se borra**, no se archiva. El
historial de git guarda lo cerrado. Un listado donde conviven cosas hechas y
pendientes deja de leerse a los dos meses.

Cada punto lleva quién lo desbloquea:

| Marca | Significa |
|---|---|
| `[código]` | Se hace entero desde un repositorio. Cero dinero, cero cuentas |
| `[tuyo]` | Necesita una decisión o una gestión que solo puede hacer el dueño |
| `[cuenta]` | Gratis en dinero, pero exige abrir una cuenta externa |
| `[$]` | Cuesta dinero |

---

## 1 · No hay dominio propio `[$]` `[tuyo]`

**Qué pasa.** El sitio vive en `panaclaw.netlify.app`.

**Qué bloquea.** Pauta pagada. Un anuncio que lleva a un subdominio de Netlify
contradice el pilar de «el sitio es tuyo» en el primer clic, y es lo primero que
nota alguien que está evaluando agencias.

**Nota del repositorio del sitio:** el dominio se compra cuando el resto de esta
lista esté resuelto, no antes — arreglarlo después sale más caro.

---

## 2 · Google Analytics 4 sin configurar `[cuenta]`

**Qué pasa.** `ga4MeasurementId` está vacío en `src/data/analytics.ts`, a
propósito: un identificador falso mediría en la cuenta de nadie y lo parecería
todo menos roto.

**Qué bloquea.**

- **Google Ads.** Sin GA4 no se puede importar la conversión, así que una campaña
  se puede correr pero no leer. Ver
  [`campanas/canales/google.md`](../campanas/canales/google.md).
- Ver el recorrido completo de alguien desde que entra hasta que envía.

**Hoy solo mide Meta**, con el píxel `1067898639025746` y el evento `Lead` en
`/gracias/`.

**Cómo se arregla.** Sacar el identificador (`G-…`) de Analytics → Administrar →
Flujos de datos y ponerlo en `src/data/analytics.ts`. **Y actualizar
`/privacidad` en el mismo commit** — la página declara qué se recoge y quién lo
recibe; si dice una cosa y el sitio hace otra, deja de ser un descuido de
redacción y pasa a ser una declaración falsa.

---

## 3 · Los cuatro proyectos están sin medir `[código]`

**Qué pasa.** Las fichas de `src/data/projects.ts` tienen nombre, dominio, enlace
y sector. No tienen métricas, ni año, ni reto, ni solución.

**Qué bloquea.** Cualquier pieza que necesite prueba. Ver
[`catalogo/09-prueba.md`](../catalogo/09-prueba.md).

**Cómo se arregla.** `npm run medir` en el repositorio del sitio saca las medidas
con su fecha. Necesita una clave gratuita de PageSpeed Insights. El contenido
—reto y solución— lo escribe quien hizo el proyecto.

**Mientras tanto:** no se publica ninguna cifra de resultado. Una ficha a medias
se ve corta pero nunca falsa.

---

## 4 · No hay identidad sonora `[tuyo]`

**Qué pasa.** La marca no tiene música, ni locutor, ni criterio de audio
definido.

**Qué bloquea.** Nada crítico: los reels y las stories se consumen sin sonido la
mayoría de las veces, y
[`prompts/video/video-corto.md`](../prompts/video/video-corto.md) está escrito
para que el video funcione mudo.

**Cuando toque decidirlo:** si hay voz, ¿es la del dueño o sintética? Es la
pregunta que hay que hacerle al humano cada vez que pida un video con voz.

---

## 5 · No hay cuentas de redes sociales `[tuyo]`

**Qué pasa.** El footer del sitio lista WhatsApp, Instagram, LinkedIn, GitHub y
X, pero **solo WhatsApp tiene enlace**. Los demás iconos salen desactivados,
porque un icono que lleva a un 404 hace más daño que un icono apagado.

**Qué bloquea.** El contenido orgánico de
[`prompts/texto/organico.md`](../prompts/texto/organico.md) no tiene dónde
publicarse todavía.

---

## Cómo se usa este documento

Cualquier agente que vaya a producir una campaña, conectar una herramienta
externa o proponer una métrica **lee esto antes**, y dice en la entrega qué punto
afecta a su trabajo.

No es una lista de excusas: es la aplicación hacia dentro de la regla 7 de la
marca —**di siempre qué no incluye**—. Entregar una campaña sin avisar de que su
canal principal todavía no se puede medir es exactamente la letra chica que esta
marca dice no tener.
