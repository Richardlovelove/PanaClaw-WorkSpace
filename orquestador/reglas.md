# Las reglas que no se negocian

Doce reglas, cada una con el motivo por el que existe. No son preferencias de
estilo: cada una tapa una forma concreta de perder un cliente o de quedar en
evidencia. Las cinco primeras son las que más caro salen y están resumidas en el
[orquestador](../CLAUDE.md#2-las-cinco-reglas-que-no-puedes-romper).

Van dirigidas al agente que produce, no al humano que revisa.

---

## 1. Ninguna cifra que no esté en `datos/precios.json`

No inventes, no redondees, no estimes, no proyectes, no conviertas a otra moneda.

El argumento entero de PanaClaw es que el precio está publicado y no cambia. Una
pieza de publicidad que anuncie $299 cuando el plan cuesta $295 no es un error de <!-- v: contraejemplo, $299 es la cifra inventada que se ilustra -->
tipeo: es la primera prueba de que sí había letra chica. Y el cliente que la ve
compara con la web, encuentra la diferencia y deja de creer todo lo demás.

**Si te falta un precio, ese producto no existe todavía.** Dilo y para.

## 2. Un pago único y una mensualidad nunca se suman

Dos totales separados, etiquetados, siempre. «$375 de una vez y $45 al mes», no <!-- v: ejemplo genérico de dos totales, no son precios del catálogo -->
«$420». <!-- v: contraejemplo, $420 es la suma prohibida -->

Lo trajo el servicio de seguridad, que cobra las dos cosas a la vez. Sumarlos da
un número perfectamente creíble y completamente falso, y proyectar la mensualidad
a doce meses para enseñar una cifra más redonda anuncia un compromiso que el
cliente no ha firmado. El cotizador del sitio lleva dos totales por esto mismo, y
tiene una prueba automática que los vigila por separado.

## 3. Cero jerga

Prohibidas, sin excepción, en cualquier texto de cara al cliente: Jamstack, CDN,
LCP, SSG, headless, stack, deploy, framework, Lighthouse, Core Web Vitals,
Supabase, Astro, «scope creep», «pipeline», «onboarding».

Permitidas porque el cliente ya las reconoce: WordPress, Google, WhatsApp,
Instagram, Facebook, Telegram, Yappy, PayPal, GitHub, Cloudflare.

**La prueba:** si una frase solo la entiende un programador, está mal escrita.
Reescríbela diciendo qué le cambia al cliente, no con qué se hace.

> Esta regla se ha roto en producción una vez: la imagen social del sitio decía
> «Sitios Jamstack en Panamá», que es lo que se ve al pegar un enlace en un
> chat. Se corrigió el 2026-08-14. Se cuenta porque enseña dónde se cuela la
> jerga: no en la página que se revisa diez veces, sino en el archivo generado
> que nadie vuelve a mirar.

## 4. Nada de datos inventados

Métricas, testimonios, casos de éxito, número de clientes, logos, premios,
años de experiencia: solo lo verificado, y las cifras con su fecha de medición.

No es prudencia decorativa. La marca vende que los números se miden; una cifra
inflada en un anuncio desmonta las otras once piezas de la campaña. Si necesitas
una prueba social y no la tienes, **usa una promesa verificable en su lugar** —
«el código queda a tu nombre» es comprobable y no requiere inventar a nadie.

Los cuatro proyectos publicados están en `catalogo/09-prueba.md` con exactamente
lo que se puede decir de cada uno, que es menos de lo que a un publicista le
gustaría.

## 5. Un solo acento cromático

Naranja `#FF5100` para todo lo que sea acento: botones, antetítulos, viñetas,
foco, el punto del wordmark.

Rojo ember `#FF1E1E` **solo en fondos**: degradados, vetas de imagen, atmósfera.
Nunca en un texto, nunca en un icono, nunca en un botón.

Y nada de azul. El azul es el color de todas las agencias tecnológicas del mundo,
y PanaClaw se posiciona explícitamente en contra de esa categoría.

## 6. El dolor antes que la herramienta

Toda frase de cara al cliente empieza por la situación en la que está la persona,
no por lo que nosotros hacemos.

Mal: «Sitios estáticos precompilados con hidratación parcial.»
Bien: «Tu sitio abre antes de que a nadie le dé tiempo a arrepentirse.»

Mal: «Autenticación con control de acceso por filas.»
Bien: «Cada persona entra con su clave y ve solo lo que le corresponde.»

## 7. Di siempre qué NO incluye

Cada producto de la marca publica su lista de exclusiones, y es deliberado: lo
que sale caro no es cobrar aparte, es que el cliente se entere después.

Aplica a lo que produzcas. Un anuncio que promete «tu web lista en 72 horas» sin
decir que el reloj empieza cuando el cliente entrega los textos está preparando
una discusión. La condición va **en la pieza**, no en la letra pequeña.

## 8. Los rangos se citan enteros

`$80–$150` se cita `$80–$150`, o `desde $80`. Nunca `$80` a secas.

El motivo del rango se dice al lado, no en una FAQ tres pantallas abajo: «no
cuesta lo mismo revisar una página de cinco secciones que una tienda con años de
complementos encima». Un rango sin su razón parece que se lo inventan sobre la
marcha.

## 9. Respeta las fronteras entre productos

Cuatro cosas de este catálogo se parecen y no son lo mismo. Confundirlas es el
error más caro que puede cometer un agente aquí, porque genera una venta que
luego no se puede cumplir:

- **Care** mantiene la infraestructura: dominio, copias, actualizaciones, caídas.
- **Seguridad** es ciberseguridad: quién entra, por dónde, y cómo impedirlo.
- **Diagnóstico de Ventas ($49)** mira el negocio: por qué el sitio no vende.
- **Auditoría de Seguridad ($80–$150)** mira por dónde te pueden entrar.

Está desarrollado en [`catalogo/08-fronteras.md`](../catalogo/08-fronteras.md).
Consúltalo antes de escribir sobre cualquiera de los cuatro.

## 10. El número de WhatsApp no se imprime

Los botones dicen «WhatsApp», sin dígitos. El número aparece cuando la persona ya
está dentro de la conversación, no como reclamo público.

Es una decisión de marca del sitio y aplica a toda pieza publicitaria: el CTA es
la acción, no el teléfono. El enlace se compone con la plantilla de
`datos/marca.json` → `contacto.plantillaEnlace`.

## 11. Ninguna promesa de posicionamiento en Google

Está prohibido prometer primeras posiciones, plazos de posicionamiento o
resultados de SEO. La postura publicada de la marca es literalmente
«no, y desconfía de quien te lo prometa».

Lo que sí se puede prometer, porque es verificable el primer día: la velocidad, y
que el sitio se entrega con todo lo necesario para que Google lo entienda.

## 12. Accesibilidad y movimiento

Solo se anima `transform` y `opacity`. `prefers-reduced-motion: reduce` apaga
todo. Ningún objetivo táctil por debajo de 24 px.

Aplica a cualquier pieza interactiva que produzcas — landing, correo, prototipo.
No es una cortesía: una web que vende abrir en menos de un segundo no puede
permitirse repintados por una animación decorativa.

---

## Cómo se comprueba

`node herramientas/verificar.mjs` vigila mecánicamente lo que se puede vigilar
mecánicamente: las reglas 1, 3, 5 y 8. Las demás son de criterio y las revisa
quien entrega.

La regla al añadir una comprobación nueva, heredada del repositorio del sitio:
**rompe lo que vigila y comprueba que salta.** Un cepo que también pasa con la
función desactivada no vigila nada.
