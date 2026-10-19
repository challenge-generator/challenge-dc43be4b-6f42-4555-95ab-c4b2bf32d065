# Guía de Accesibilidad

Esta guía establece los criterios de accesibilidad basados en WCAG 2.2 para garantizar que todos los componentes y flujos de usuario sean accesibles para personas con discapacidades. Los criterios se aplican a todos los artefactos de diseño generados en este proyecto.

## 1. Perceptible

### 1.1 Alternativas Textuales
- **Criterio 1.1.1 Contenido no textual (Nivel A)**:
  - Todos los íconos, imágenes y elementos gráficos deben tener una alternativa textual descriptiva.
  - Ejemplo: Un botón con icono de "guardar" debe incluir un `aria-label="Guardar"` o texto visible equivalente.
  - Los placeholders en campos de formulario no deben usarse como única alternativa textual.

### 1.2 Adaptable
- **Criterio 1.3.1 Información y relaciones (Nivel A)**:
  - La estructura semántica (encabezados, listas, tablas) debe ser clara y coherente.
  - Ejemplo: Usar etiquetas `<h1>` a `<h6>` para jerarquía de títulos en documentación.
  - Los formularios deben asociar etiquetas con campos usando `<label>` o `aria-labelledby`.

- **Criterio 1.3.2 Secuencia significativa (Nivel A)**:
  - El orden de lectura en pantallas debe ser lógico y seguir el flujo visual.
  - Verificar con herramientas como NVDA o VoiceOver.

- **Criterio 1.3.4 Orientación (Nivel AA)**:
  - Los diseños deben ser funcionales tanto en orientación horizontal como vertical.

- **Criterio 1.3.5 Identificar el propósito de entrada (Nivel AA)**:
  - Los campos de formulario deben usar `autocomplete` para ayudar a usuarios con discapacidades cognitivas.
  - Ejemplo: `autocomplete="name"` para campos de nombre.

### 1.3 Distinguible
- **Criterio 1.4.1 Uso del color (Nivel A)**:
  - El color no debe ser el único medio para transmitir información.
  - Ejemplo: Un mensaje de error debe incluir un icono o texto además del color rojo.

- **Criterio 1.4.3 Contraste mínimo (Nivel AA)**:
  - Texto normal debe tener un contraste mínimo de 4.5:1 con su fondo.
  - Texto grande (mayor a 18.66px o 14px en negrita) debe tener un contraste de 3:1.
  - Herramientas recomendadas: [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/).

- **Criterio 1.4.4 Cambio de tamaño del texto (Nivel AA)**:
  - El texto debe poder ampliarse hasta un 200% sin pérdida de funcionalidad.

- **Criterio 1.4.10 Reflujo (Nivel AA)**:
  - El contenido debe adaptarse a pantallas de 320px de ancho sin necesidad de desplazamiento horizontal.

- **Criterio 1.4.11 Contraste de componentes no textuales (Nivel AA)**:
  - Componentes interactivos (botones, iconos) deben tener un contraste de 3:1 con su fondo.

- **Criterio 1.4.12 Espaciado del texto (Nivel AA)**:
  - Los usuarios deben poder ajustar el espaciado entre líneas, párrafos y palabras sin perder contenido.

- **Criterio 1.4.13 Contenido al pasar el cursor o enfocar (Nivel AA)**:
  - El contenido adicional que aparece al pasar el cursor (tooltips) debe ser:
    - Cerrarse con la tecla `Esc`.
    - Permanecer visible mientras el cursor esté sobre él.
    - No obstruir otro contenido.

## 2. Operable

### 2.1 Accesible por Teclado
- **Criterio 2.1.1 Teclado (Nivel A)**:
  - Toda la funcionalidad debe ser operable mediante teclado.
  - Ejemplo: Los menús desplegables deben abrirse con `Espacio` o `Enter`.

- **Criterio 2.1.2 Sin trampas para el teclado (Nivel A)**:
  - El foco no debe quedar atrapado en ningún componente.

- **Criterio 2.1.4 Atajos de teclado (Nivel A)**:
  - Si se implementan atajos de teclado, deben ser:
    - Desactivables.
    - Reconfigurables.
    - No entrar en conflicto con atajos del navegador.

### 2.2 Tiempo Suficiente
- **Criterio 2.2.1 Tiempo ajustable (Nivel A)**:
  - Los temporizadores (ej. sesiones) deben poder extenderse o desactivarse.

- **Criterio 2.2.2 Pausar, detener, ocultar (Nivel A)**:
  - Los movimientos automáticos (ej. carruseles) deben poder pausarse.

### 2.3 Convulsiones y Reacciones Físicas
- **Criterio 2.3.1 Umbral de tres destellos (Nivel A)**:
  - Evitar contenido que destelle más de tres veces por segundo.

### 2.4 Navegable
- **Criterio 2.4.1 Omitir bloques (Nivel A)**:
  - Proporcionar un mecanismo para omitir contenido repetitivo (ej. menús).

- **Criterio 2.4.2 Título de página (Nivel A)**:
  - Cada pantalla debe tener un título descriptivo y único.

- **Criterio 2.4.3 Orden del foco (Nivel A)**:
  - El orden del foco al navegar con teclado debe ser lógico.

- **Criterio 2.4.4 Propósito del enlace (Nivel A)**:
  - El texto del enlace debe describir su propósito sin contexto adicional.
  - Ejemplo: Evitar "Haz clic aquí". Usar "Descargar informe anual".

- **Criterio 2.4.5 Múltiples vías (Nivel AA)**:
  - Proporcionar más de una forma de localizar una página (ej. menú, buscador, mapa del sitio).

- **Criterio 2.4.6 Encabezados y etiquetas (Nivel AA)**:
  - Los encabezados y etiquetas deben ser descriptivos.

- **Criterio 2.4.7 Foco visible (Nivel AA)**:
  - El indicador de foco debe ser claramente visible.
  - Usar el token `neutral.border.focus` para el borde de foco.

- **Criterio 2.4.11 Enfoque no obstruido (Nivel AA)**:
  - El foco no debe quedar oculto por otros elementos.

## 3. Comprensible

### 3.1 Legible
- **Criterio 3.1.1 Idioma de la página (Nivel A)**:
  - Especificar el idioma de la página (ej. `lang="es"`).

- **Criterio 3.1.2 Idioma de las partes (Nivel AA)**:
  - Indicar el idioma de fragmentos en otro idioma (ej. `lang="en"`).

### 3.2 Predecible
- **Criterio 3.2.1 Al enfocar (Nivel A)**:
  - Enfocar un elemento no debe desencadenar cambios de contexto inesperados.

- **Criterio 3.2.2 Al ingresar datos (Nivel A)**:
  - Ingresar datos no debe desencadenar cambios de contexto sin advertencia.

- **Criterio 3.2.3 Navegación coherente (Nivel AA)**:
  - Los mecanismos de navegación deben aparecer en el mismo orden relativo en todas las pantallas.

- **Criterio 3.2.4 Identificación coherente (Nivel AA)**:
  - Componentes con la misma funcionalidad deben identificarse consistentemente.

### 3.3 Asistencia de Entrada
- **Criterio 3.3.1 Identificación de errores (Nivel A)**:
  - Los errores deben identificarse claramente y sugerir correcciones.

- **Criterio 3.3.2 Etiquetas o instrucciones (Nivel A)**:
  - Proporcionar etiquetas o instrucciones para campos de formulario.

- **Criterio 3.3.3 Sugerencias ante errores (Nivel AA)**:
  - Proporcionar sugerencias para corregir errores (ej. formato de fecha).

- **Criterio 3.3.4 Prevención de errores (Nivel AA)**:
  - Para acciones irreversibles (ej. borrar datos), proporcionar:
    - Confirmación.
    - Revisión.
    - Reversión.

## 4. Robusto

### 4.1 Compatible
- **Criterio 4.1.1 Análisis sintáctico (Nivel A)**:
  - El marcado debe ser válido y sin errores.

- **Criterio 4.1.2 Nombre, función, valor (Nivel A)**:
  - Todos los componentes deben tener un nombre, función y valor accesibles para tecnologías de asistencia.
  - Ejemplo: Usar `aria-label`, `aria-role` y `aria-hidden` correctamente.

- **Criterio 4.1.3 Mensajes de estado (Nivel AA)**:
  - Los mensajes de estado (ej. notificaciones) deben ser reconocibles por tecnologías de asistencia sin recibir foco.
  - Ejemplo: Usar `aria-live="polite"` para notificaciones.

## Verificación de Accesibilidad

### Herramientas Recomendadas
- [WAVE Evaluation Tool](https://wave.webaim.org/): Para evaluar contraste, estructura y alternativas textuales.
- [axe DevTools](https://www.deque.com/axe/): Extensión para Chrome que identifica problemas de accesibilidad.
- [NVDA](https://www.nvaccess.org/): Lector de pantalla gratuito para Windows.
- [VoiceOver](https://support.apple.com/es-es/guide/voiceover/welcome/10): Lector de pantalla integrado en macOS.
- [Color Contrast Analyzer](https://www.tpgi.com/color-contrast-checker/): Para verificar contraste de colores.

### Proceso de Verificación
1. **Revisión Automática**: Usar herramientas como WAVE o axe para identificar problemas básicos.
2. **Revisión Manual**:
   - Navegar usando solo el teclado.
   - Verificar contraste de colores.
   - Probar con lectores de pantalla.
3. **Pruebas con Usuarios**: Involucrar a usuarios con discapacidades en pruebas de usabilidad.

### Lista de Verificación Rápida
- [ ] Todos los elementos no textuales tienen alternativas textuales.
- [ ] El contraste de texto y componentes cumple con WCAG 2.2.
- [ ] La interfaz es operable mediante teclado.
- [ ] El orden del foco es lógico.
- [ ] Los encabezados siguen una jerarquía clara.
- [ ] Los formularios tienen etiquetas asociadas.
- [ ] Los mensajes de error son claros y ofrecen sugerencias.
- [ ] El contenido es adaptable a diferentes tamaños de pantalla.

## Ejemplos de Implementación

### Ejemplo 1: Botón Accesible
```html
<button
  class="btn-primary"
  aria-label="Guardar cambios"
  aria-disabled="false"
  style="
    background-color: var(--color-primary-default);
    color: white;
    padding: var(--spacing-md) var(--spacing-lg);
    border-radius: var(--borderRadius-md);
    border: none;
    font-size: var(--typography-fontSize-body-medium);
    font-weight: var(--typography-fontWeight-medium);
  "
>
  Guardar
</button>
```

### Ejemplo 2: Campo de Formulario Accesible
```html
<label for="email">Correo Electrónico</label>
<input
  type="email"
  id="email"
  name="email"
  autocomplete="email"
  aria-describedby="email-hint"
  style="
    padding: var(--spacing-sm);
    border: 1px solid var(--color-neutral-border-default);
    border-radius: var(--borderRadius-sm);
    font-size: var(--typography-fontSize-body-medium);
  "
>
<span id="email-hint" style="font-size: var(--typography-fontSize-label-small); color: var(--color-neutral-text-secondary);">
  Ejemplo: usuario@ejemplo.com
</span>
```

### Ejemplo 3: Notificación Accesible
```html
<div
  role="alert"
  aria-live="assertive"
  style="
    background-color: var(--color-error-default);
    color: white;
    padding: var(--spacing-md);
    border-radius: var(--borderRadius-md);
    margin: var(--spacing-md) 0;
  "
>
  Error: El correo electrónico no es válido.
</div>
```

## Recursos Adicionales
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [Guía de Accesibilidad Web de Google](https://developers.google.com/web/fundamentals/accessibility)
- [Material Design Accessibility](https://m3.material.io/foundations/accessible-design/overview)
- [WebAIM](https://webaim.org/)