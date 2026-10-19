# Optimización y Uso Avanzado de Herramientas de Diseño UI

El equipo de diseño de soluciones de una empresa fintech necesita un Product Designer avanzado que pueda optimizar el trabajo mediante la creación y uso de librerías de componentes y funciones avanzadas de las herramientas de diseño UI. El candidato debe demostrar su habilidad para diseñar interfaces eficientes y reutilizables que mejoren la experiencia del usuario y la eficiencia del equipo.

## Informacion General

| Campo | Valor |
|-------|-------|
| **Tema** | Dominio avanzado de herramientas de diseño UI |
| **Nivel** | advanced-l2 |
| **Tipo** | practical |
| **Tiempo estimado** | 10 horas |

## Fases del Reto

### Fase 0: Configuración del Proyecto

**Objetivo:** Obtener el proyecto base funcional enviando el Código Base a un asistente de IA, que lo analizará, corregirá errores y generará un ZIP listo para usar.

**Tiempo estimado:** 15-30 minutos

**Instrucciones:**

- Asegúrate de tener instalado para ejecutar el proyecto: Un IDE o editor de código.
- Copia todo el contenido del campo **Código Base** de este reto — incluyendo el texto de instrucciones que aparece al inicio.
- Abre un asistente de IA (Claude en claude.ai, ChatGPT o Gemini — se recomienda Claude), pega el contenido copiado en el chat y envíalo.
- El asistente analizará los archivos, corregirá errores y generará un archivo ZIP descargable. Descárgalo y extráelo en la carpeta donde quieras trabajar.
- Verifica que el proyecto arranca sin errores.

**Entregable:** El proyecto compila/arranca sin errores.

<details>
<summary>Pistas de conocimiento</summary>

- Copia el Código Base completo incluyendo el texto de instrucciones al inicio — esas instrucciones le indican al asistente exactamente qué hacer con los archivos.
- Si el asistente no genera el ZIP automáticamente al terminar el análisis, escríbele: "genera el ZIP ahora".
- Si el proyecto tiene errores al arrancar, comparte el mensaje de error con el mismo asistente para que lo corrija.

</details>

### Fase 1: Creación de una librería de componentes

**Objetivo:** Diseñar y documentar una librería de componentes reutilizables para la empresa.

**Tiempo estimado:** 4 horas

**Instrucciones:**

- Identifica los componentes UI más utilizados en la empresa.
- Diseña una librería de componentes que incluya al menos 10 elementos reutilizables.
- Documenta cada componente con ejemplos de uso y mejores prácticas.

**Entregable:** Librería de componentes documentada.

<details>
<summary>Pistas de conocimiento</summary>

- Considera la consistencia visual y funcional de los componentes.
- Piensa en la escalabilidad y mantenibilidad de la librería.

</details>

### Fase 2: Uso de funciones avanzadas de las herramientas de diseño UI

**Objetivo:** Demostrar el uso de funciones avanzadas de las herramientas de diseño UI para mejorar la eficiencia y la calidad del diseño.

**Tiempo estimado:** 3 horas

**Instrucciones:**

- Selecciona una herramienta de diseño UI que domines.
- Identifica al menos 5 funciones avanzadas de la herramienta.
- Crea un diseño UI que utilice estas funciones para mejorar la eficiencia y la calidad del diseño.

**Entregable:** Diseño UI que utiliza funciones avanzadas de la herramienta de diseño.

<details>
<summary>Pistas de conocimiento</summary>

- Explora las capacidades de la herramienta para automatizar tareas y mejorar la eficiencia.
- Considera cómo las funciones avanzadas pueden mejorar la calidad del diseño y la experiencia del usuario.

</details>

### Fase 3: Evaluación y mejora continua de la librería de componentes

**Objetivo:** Evaluar y mejorar continuamente la librería de componentes para asegurar su relevancia y efectividad.

**Tiempo estimado:** 3 horas

**Instrucciones:**

- Recopila feedback de los usuarios de la librería.
- Identifica áreas de mejora y realiza los cambios necesarios.
- Documenta los cambios y mejoras realizadas.

**Entregable:** Librería de componentes actualizada y documentada.

<details>
<summary>Pistas de conocimiento</summary>

- Considera la usabilidad y la accesibilidad de los componentes.
- Piensa en cómo puedes hacer que la librería sea más fácil de mantener y actualizar.

</details>

## Dimensiones Evaluadas

- **queEs**: ¿Qué es una librería de componentes UI y por qué es importante en el diseño de soluciones?
- **paraQueSirve**: ¿Para qué sirve el uso de funciones avanzadas de las herramientas de diseño UI en el proceso de diseño?
- **comoSeUsa**: ¿Cómo se puede utilizar una librería de componentes UI para mejorar la eficiencia y la calidad del diseño?
- **erroresComunes**: ¿Cuáles son los errores comunes al crear y mantener una librería de componentes UI?
- **queDecisionesImplica**: ¿Qué decisiones implica la evaluación y mejora continua de una librería de componentes UI?

## Criterios de Evaluacion

- Creación de una librería de componentes UI documentada.
- Uso de funciones avanzadas de las herramientas de diseño UI para mejorar la eficiencia y la calidad del diseño.
- Evaluación y mejora continua de la librería de componentes UI.

## Como trabajar con un asistente de IA

Hay dos caminos, elegi uno:

- **AGENTS.md** (recomendado) — instrucciones nativas del repo. Abri esta carpeta con tu agente local (Claude Code, Cursor, Codex, Copilot, Gemini) y las carga solo. Sabe que archivos faltan y con que comando se verifica, y completa el scaffold escribiendo en disco.
- **PROMPT_MEJORA.md** — para copiar y pegar en un chat (claude.ai, ChatGPT). Devuelve un ZIP con el proyecto. Sirve si no tenes un agente en el IDE.

Ninguno de los dos resuelve las fases del reto: eso es tu trabajo.

## Verificacion

El proyecto esta listo para trabajar cuando este comando corre sin errores:

```bash
python3 -c "import json; json.load(open('design-tokens.json'))"
```

---

*Reto generado automaticamente por Challenge Generator - Pragma*
