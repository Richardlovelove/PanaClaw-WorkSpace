# Canal · Meta (Facebook e Instagram)

El canal principal hoy: es el único con medición activa.

---

## Estado de la medición

- **Píxel de Meta activo:** `1067898639025746`, desde 2026-08-03
- **Eventos:** `PageView` en cada página, y **`Lead` solo en `/gracias/`**
- `/gracias/` es el único punto del sitio donde alguien ha completado algo, así
  que es el único evento que sirve para medir conversiones y construir públicos
  parecidos

**Consecuencia:** toda campaña de Meta se optimiza contra `Lead`. Un objetivo de
«tráfico» desperdicia el píxel.

---

## Formatos

| Ubicación | Proporción | Píxeles |
|---|---|---|
| Feed (recomendado) | 4:5 | 1080 × 1350 |
| Feed cuadrado | 1:1 | 1080 × 1080 |
| Stories y Reels | 9:16 | 1080 × 1920 |

**4:5 por defecto:** ocupa más pantalla en el feed móvil que el cuadrado y no
sufre el recorte de las historias.

---

## Los primeros 125 caracteres

Es el anuncio entero. Después viene el «ver más», y casi nadie lo pulsa.

**Ahí tienen que estar el gancho y la cifra.** El giro y el límite pueden caer
después.

```
Tu web tarda y la gente se va antes de ver lo que vendes. $295, lista en 72 h.
```

78 caracteres, y ya está todo lo esencial.

---

## Públicos

### Frío

- **Ubicación:** Panamá
- **Edad:** 25–55
- **Intereses:** dueños de pequeñas empresas, emprendimiento, comercio local
- **No segmentes por «diseño web» ni «tecnología»**: eso alcanza a colegas del
  sector, no a clientes

### Tibio — remarketing de sitio

Requiere el píxel, que ya está. Públicos útiles:

| Público | Qué anuncia |
|---|---|
| Visitó `/planes/` sin llegar a `/gracias/` | La objeción del precio, o el cotizador |
| Visitó `/ebot/` | Los dos costos de terceros, publicados |
| Visitó `/seguridad/` | El procedimiento de los cuatro pasos |
| Visitó `/cotizador/` sin enviar | Una promesa: el código queda a tu nombre |

### Parecidos (lookalike)

**Todavía no.** Hacen falta suficientes eventos `Lead` para que el público
parecido signifique algo. Con el sitio en beta y sin campañas corridas, un
lookalike hoy se construye sobre ruido.

---

## Lo que Meta va a empujar y hay que rechazar

La plataforma sugiere activamente cosas que rompen esta marca:

| Meta sugiere | Por qué no |
|---|---|
| Añadir emojis al texto | Prohibido en la marca |
| «Mejorar» el copy con su IA | Mete exclamaciones y relleno de agencia |
| Recortar la imagen a otras proporciones automáticamente | Parte el sujeto y tapa el hueco del titular |
| Añadir un botón de «Reservar ahora» | El CTA se elige a propósito |
| Ventajas+ con creativo automático | Reencuadra, aplica filtros y cambia el color |

**Desactiva las mejoras automáticas de creativo.** Con un sistema visual de negro
y un solo acento, cualquier ajuste automático de brillo o saturación lo rompe.

---

## Presupuesto y lectura

No hay histórico de esta marca, así que cualquier cifra de referencia sería
inventada. Lo que sí se puede decir:

- **Una prueba en frío necesita al menos 4 variantes** con hipótesis distintas
  (ver [`plantillas/estructura-anuncio.md`](../plantillas/estructura-anuncio.md)).
- **No se lee nada antes de tener eventos suficientes.** Un ganador declarado con
  tres conversiones es ruido.
- **Lo que se mide es `Lead`**, no clics ni alcance.

---

## Antes de subir

- [ ] ¿Gancho y cifra dentro de los primeros 125 caracteres?
- [ ] ¿4:5 para feed?
- [ ] ¿El texto de la story queda fuera de las zonas seguras?
- [ ] ¿Mejoras automáticas de creativo desactivadas?
- [ ] ¿El objetivo está puesto en `Lead` y no en tráfico?
- [ ] ¿La cifra coincide con `datos/precios.json`?
- [ ] ¿El CTA de WhatsApp va sin número?
