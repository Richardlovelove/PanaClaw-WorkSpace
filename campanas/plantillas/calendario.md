# Plantilla · Calendario

Cómo se reparte un mes de contenido sin repetirse y sin inventar nada.

---

## La rejilla mensual

Una publicación cada tres días = **10 al mes**. Es un ritmo sostenible para una
agencia de una persona y suficiente para que el argumento se acumule.

| # | Tipo | Producto / tema |
|---|---|---|
| 1 | Cifra publicada | Plan del mes |
| 2 | Desastre explicado | Pilar velocidad |
| 3 | Objeción contestada | La principal del público del mes |
| 4 | Cifra publicada | Una condición (rondas, plazos, forma de cobro) |
| 5 | Frontera | Dos productos que se confunden |
| 6 | Desastre explicado | Pilar seguridad |
| 7 | Objeción contestada | Otra del mismo público |
| 8 | Trabajo enseñado | Uno de los cuatro proyectos |
| 9 | Cifra publicada | Otro producto del catálogo |
| 10 | Desastre explicado | Pilar entrega en días |

Los tipos están definidos en
[`prompts/texto/organico.md`](../../prompts/texto/organico.md).

---

## Por qué el material no se acaba

Es la pregunta que mata a cualquier calendario de contenido. Con esta marca hay
inventario real, sin inventar nada:

| Fuente | Piezas disponibles |
|---|---|
| Productos con precio publicado | 6 |
| Listas de «qué no incluye» | 5 |
| Objeciones catalogadas | ~20 |
| Fronteras entre productos | 5 |
| Pilares y pasos del proceso | 6 |
| Proyectos publicados | 4 |
| Condiciones comerciales | ~8 |

**Más de 50 publicaciones posibles**, todas verificables. A diez al mes, medio
año sin repetirse.

---

## Un mes, con foco

Cada mes se elige **un público** de
[`adn/04-audiencia.md`](../../adn/04-audiencia.md) y el contenido gira alrededor
de él. No se rota entre seis públicos dentro del mismo mes: nadie construye
argumento así.

```
Mes 1   El que no tiene sitio          → Start, Diagnóstico
Mes 2   El WordPress que da vergüenza  → Diagnóstico, Corporate
Mes 3   El que no da abasto            → eBot
Mes 4   El que no sabe si está expuesto→ Auditoría
```

Los cuatro públicos restantes entran cuando los primeros hayan dado datos.

---

## Cómo se cruza con la pauta

| | Orgánico | Pauta |
|---|---|---|
| Función | Construir el argumento | Comprar la atención |
| Ritmo | 10 al mes | Continua mientras haya presupuesto |
| Llamada a la acción | 1 de cada 3 como mucho | Siempre |
| Público | El mismo del mes | El mismo del mes |

**El anuncio y el contenido del mes hablan del mismo público.** Un anuncio de
eBot mientras el orgánico habla de seguridad son dos campañas a medias.

---

## La ficha de un mes

```
MES
  Público del mes
  Producto principal
  Producto secundario
  Ángulo                        UNO

ORGÁNICO
  10 publicaciones, con su tipo y su tema

PAUTA
  Campaña fría        producto, ángulo, destino, piezas
  Campaña tibia       objeción que ataca, destino, piezas
  Remarketing         la promesa, destino

PRODUCCIÓN
  Piezas visuales nuevas       cuántas y de qué escena madre
  Piezas derivadas de encuadre cuántas
  Lo que NO se puede producir  y por qué
```

El último campo es obligatorio. Si tres piezas del mes dependen de una métrica
que no está medida o de una foto que no existe, se dice **al entregar el
calendario**, no cuando toque producirlas.

---

## Antes de aprobar un calendario

- [ ] ¿Un solo público en el mes?
- [ ] ¿Un solo ángulo?
- [ ] ¿El orgánico y la pauta hablan del mismo público?
- [ ] ¿Alguna pieza necesita un dato que no existe?
- [ ] ¿Se repite algún tema del mes anterior?
- [ ] ¿Están las cifras verificadas contra `datos/precios.json`?
