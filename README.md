# PanaClaw Workspace

El cerebro de la marca **PanaClaw**, agencia de sitios web en Panamá.

No es un proyecto de software: no se compila, no se despliega y no tiene
interfaz. Es una base de conocimiento pensada para que **cualquier agente de IA**
—Claude, Grok, Gemini, Pomelli, Canva— entre, entienda la marca en una sola
lectura y devuelva un entregable que suene, se vea y cobre exactamente como
PanaClaw.

> **Si eres un agente, empieza por [`CLAUDE.md`](CLAUDE.md).** Trae las reglas
> duras y la tabla que te manda al resto según lo que te hayan pedido.

---

## Para qué sirve

Le pides a una IA «prompts de Nano Banana para la campaña de eBot», «cuatro
anuncios para Meta» o «una propuesta para este cliente», y sale con los precios
correctos, los hex correctos, la voz correcta y —lo más difícil— **diciendo qué
no incluye**, que es la firma de la marca.

---

## Cómo está organizado

```
CLAUDE.md         ← El orquestador. Punto de entrada de cualquier agente.

datos/            Las dos fuentes de verdad. Máquina antes que prosa.
  precios.json      Toda cifra que la marca puede decir en voz alta
  marca.json        Todo token visual: hex, fuentes, formas, movimiento

adn/              Quién es la marca. Se lee antes de escribir una palabra.
  01-identidad · 02-voz-y-tono · 03-sistema-visual · 04-audiencia

catalogo/         Qué vende, en prosa. Capa legible sobre precios.json.
  Los seis productos + condiciones, fronteras y prueba

prompts/          ESTRUCTURAS de prompt. No guiones.
  bloques/          Fragmentos que se copian literales en cada pieza
  imagen/ video/ texto/
  plataformas/      Pomelli, Grok, Canva

campanas/         Embudo, plantillas de pieza y notas por canal
skills/           Procedimientos empaquetados para agentes
orquestador/      Reglas duras, enrutador y protocolo de entrega
herramientas/     verificar.mjs
operacion/        Sincronización con el sitio y deuda conocida
```

**Jerarquía de autoridad**, cuando dos archivos se contradigan:

```
datos/*.json  →  adn/*  →  catalogo/*  →  todo lo demás
```

---

## Comprobar que está al día

```bash
node herramientas/verificar.mjs
```

Sin dependencias. Vigila que ninguna cifra se haya salido de `precios.json`,
ningún hex de `marca.json`, que no se cuele jerga y que no haya enlaces rotos.
Detalles en [`herramientas/README.md`](herramientas/README.md).

---

## Relación con el repositorio del sitio

El sitio vive en **`Richardlovelove/PanaClaw`** (Astro estático en Netlify) y es
la fuente original de casi todo lo que hay aquí: los precios salen de
`src/data/*.ts` y los tokens de `src/styles/global.css`.

**Esto es un espejo, no una copia paralela.** El mapeo archivo a archivo y el
procedimiento están en
[`operacion/sincronizacion.md`](operacion/sincronizacion.md).

---

## Antes de arrancar una campaña

Lee [`operacion/deuda-conocida.md`](operacion/deuda-conocida.md). Hay tres cosas
abiertas que afectan directamente a cualquier trabajo de marketing:

1. **La imagen social del sitio lleva un nombre de marca anterior** — es lo que
   se ve al compartir cualquier enlace, y lo que van a leer las herramientas que
   deducen la marca rastreando el sitio
2. **No hay dominio propio** todavía
3. **Google Analytics sin configurar** — hoy solo mide Meta

---

## Qué NO es este repositorio

- **No es un almacén de guiones escritos.** No hay copys finales guardados. Hay
  estructuras: el copy se genera cada vez, contra el ADN, para el contexto
  concreto.
- **No es un histórico.** Lo que deja de ser cierto se borra. El historial de git
  ya guarda lo viejo.
- **No es documentación del código del sitio.** Eso está en el otro repositorio.
