# Especificación de Componentes Reutilizables

Esta especificación detalla los componentes reutilizables diseñados para el sistema de diseño de la empresa fintech. Cada componente incluye su descripción, variantes, estados, ejemplos de uso y criterios de accesibilidad según WCAG 2.2.

Los componentes siguen los principios de Atomic Design y utilizan los design tokens definidos en `foundations/design-tokens.json` como fuente única de verdad para estilos.

---

## 1. Button

### Descripción
Componente interactivo que permite a los usuarios realizar acciones. Se utiliza en formularios, diálogos y flujos de navegación.

### Variantes
- **Primary**: Acción principal de la pantalla (ej. "Enviar solicitud").
- **Secondary**: Acción secundaria (ej. "Cancelar").
- **Tertiary**: Acción menos relevante (ej. "Ver términos y condiciones").
- **Danger**: Acción destructiva (ej. "Eliminar cuenta").

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial del botón.                                                   | Botón en un formulario.                |
| Hover      | El cursor está sobre el botón.                                              | Cambio de color al pasar el cursor.    |
| Focus      | El botón está enfocado (navegación por teclado).                           | Navegación con `Tab`.                  |
| Disabled   | El botón no es interactivo.                                                 | Botón deshabilitado hasta completar un campo. |
| Error      | Indica que la acción no puede completarse debido a un error.               | Campo de formulario con error.         |
| Loading    | Indica que la acción está en proceso.                                       | Envío de un formulario.                |

### Ejemplo de Uso
```yaml
# Ejemplo en un formulario de solicitud de préstamo
- type: Button
  variant: Primary
  text: "Solicitar préstamo"
  state: Default
  action: submitLoanApplication()
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA (mínimo 4.5:1 para texto).
- **Foco**: Visible y claro para navegación por teclado.
- **Etiqueta**: Texto descriptivo y claro.
- **Redimensionamiento**: El texto se escala hasta 200% sin pérdida de funcionalidad.

---

## 2. Input

### Descripción
Campo de entrada que permite a los usuarios ingresar datos. Se utiliza en formularios y filtros.

### Variantes
- **Text**: Entrada de texto genérico.
- **Password**: Entrada de contraseñas (oculta caracteres).
- **Number**: Entrada de números (con validación).
- **Email**: Entrada de correos electrónicos (con validación básica).
- **Search**: Campo de búsqueda con icono de lupa.

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial del campo.                                                   | Campo vacío en un formulario.          |
| Hover      | El cursor está sobre el campo.                                              | Cambio de borde al pasar el cursor.    |
| Focus      | El campo está enfocado (navegación por teclado).                           | Navegación con `Tab`.                  |
| Disabled   | El campo no es interactivo.                                                 | Campo deshabilitado hasta seleccionar una opción. |
| Error      | Indica que el valor ingresado no es válido.                                | Campo con mensaje de error.            |
| Success    | Indica que el valor ingresado es válido.                                   | Campo con icono de validación.         |

### Ejemplo de Uso
```yaml
# Ejemplo en un formulario de registro
- type: Input
  variant: Email
  label: "Correo electrónico"
  placeholder: "ejemplo@dominio.com"
  state: Default
  validation: emailFormat
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA para bordes y texto.
- **Foco**: Visible y claro para navegación por teclado.
- **Etiqueta**: Asociada correctamente con `aria-label` o `label` visible.
- **Validación**: Mensajes de error claros y descriptivos.
- **Redimensionamiento**: El texto y los bordes se escalan hasta 200%.

---

## 3. Checkbox

### Descripción
Componente que permite a los usuarios seleccionar una o varias opciones de una lista.

### Variantes
- **Single**: Selección única (ej. "Acepto los términos y condiciones").
- **Group**: Grupo de opciones (ej. "Intereses: Viajes, Tecnología, Deportes").

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial del checkbox.                                                | Checkbox sin seleccionar.              |
| Hover      | El cursor está sobre el checkbox.                                           | Cambio de color al pasar el cursor.    |
| Focus      | El checkbox está enfocado (navegación por teclado).                        | Navegación con `Tab`.                  |
| Disabled   | El checkbox no es interactivo.                                              | Checkbox deshabilitado.                |
| Checked    | El checkbox está seleccionado.                                              | Opción seleccionada.                   |
| Error      | Indica que la selección es obligatoria y no se ha realizado.               | Checkbox con mensaje de error.         |

### Ejemplo de Uso
```yaml
# Ejemplo en un formulario de preferencias
- type: Checkbox
  variant: Group
  label: "Preferencias de notificaciones"
  options:
    - "Correo electrónico"
    - "SMS"
    - "Push"
  state: Default
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA para el borde y la marca de selección.
- **Foco**: Visible y claro para navegación por teclado.
- **Etiqueta**: Cada opción tiene una etiqueta descriptiva asociada.
- **Redimensionamiento**: El checkbox y su etiqueta se escalan hasta 200%.

---

## 4. Radio Button

### Descripción
Componente que permite a los usuarios seleccionar una opción de un conjunto de opciones mutuamente excluyentes.

### Variantes
- **Single**: Selección única (ej. "Método de pago: Tarjeta o Transferencia").
- **Group**: Grupo de opciones (ej. "Género: Hombre, Mujer, Otro").

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial del radio button.                                            | Radio button sin seleccionar.          |
| Hover      | El cursor está sobre el radio button.                                       | Cambio de color al pasar el cursor.    |
| Focus      | El radio button está enfocado (navegación por teclado).                    | Navegación con `Tab`.                  |
| Disabled   | El radio button no es interactivo.                                          | Radio button deshabilitado.            |
| Selected   | El radio button está seleccionado.                                          | Opción seleccionada.                   |
| Error      | Indica que la selección es obligatoria y no se ha realizado.               | Radio button con mensaje de error.     |

### Ejemplo de Uso
```yaml
# Ejemplo en un formulario de suscripción
- type: Radio Button
  variant: Group
  label: "Plan de suscripción"
  options:
    - "Básico (Gratis)"
    - "Premium ($9.99/mes)"
    - "Empresarial ($29.99/mes)"
  state: Default
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA para el borde y el punto de selección.
- **Foco**: Visible y claro para navegación por teclado.
- **Etiqueta**: Cada opción tiene una etiqueta descriptiva asociada.
- **Redimensionamiento**: El radio button y su etiqueta se escalan hasta 200%.

---

## 5. Select (Dropdown)

### Descripción
Componente que permite a los usuarios seleccionar una opción de una lista desplegable.

### Variantes
- **Single**: Selección única (ej. "País de residencia").
- **Multiple**: Selección múltiple (ej. "Intereses").

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial del select.                                                  | Select sin opción seleccionada.        |
| Hover      | El cursor está sobre el select.                                             | Cambio de borde al pasar el cursor.    |
| Focus      | El select está enfocado (navegación por teclado).                           | Navegación con `Tab`.                  |
| Disabled   | El select no es interactivo.                                                | Select deshabilitado.                  |
| Open       | La lista desplegable está abierta.                                          | Selección de una opción.               |
| Error      | Indica que la selección es obligatoria y no se ha realizado.               | Select con mensaje de error.           |

### Ejemplo de Uso
```yaml
# Ejemplo en un formulario de perfil
- type: Select
  variant: Single
  label: "País de residencia"
  options:
    - "Argentina"
    - "Brasil"
    - "Chile"
    - "Colombia"
    - "México"
  state: Default
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA para bordes y texto.
- **Foco**: Visible y claro para navegación por teclado.
- **Etiqueta**: Asociada correctamente con `aria-label` o `label` visible.
- **Navegación**: Las opciones son navegables con teclado (flechas, `Enter`).
- **Redimensionamiento**: El texto y los bordes se escalan hasta 200%.

---

## 6. Card

### Descripción
Componente que agrupa información relacionada y acciones asociadas. Se utiliza para mostrar resúmenes de contenido o acciones.

### Variantes
- **Default**: Tarjeta estándar con título, contenido y acciones.
- **Featured**: Tarjeta destacada con contenido importante (ej. "Préstamo aprobado").
- **Compact**: Tarjeta con información mínima (ej. resumen de transacción).

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial de la tarjeta.                                               | Tarjeta en una lista.                  |
| Hover      | El cursor está sobre la tarjeta.                                            | Cambio de sombra al pasar el cursor.   |
| Focus      | La tarjeta está enfocada (navegación por teclado).                          | Navegación con `Tab`.                  |
| Disabled   | La tarjeta no es interactiva.                                               | Tarjeta deshabilitada.                 |

### Ejemplo de Uso
```yaml
# Ejemplo en un dashboard de préstamos
- type: Card
  variant: Featured
  title: "Préstamo aprobado"
  content: "Tu préstamo de $5,000 ha sido aprobado. ¡Felicidades!"
  actions:
    - "Ver detalles"
    - "Descargar contrato"
  state: Default
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA para texto y bordes.
- **Foco**: Visible y claro para navegación por teclado.
- **Estructura**: Semántica correcta (`<article>`, `<section>` o equivalente).
- **Redimensionamiento**: El contenido se escala hasta 200% sin pérdida de información.

---

## 7. Alert

### Descripción
Componente que muestra mensajes importantes a los usuarios, como confirmaciones, advertencias o errores.

### Variantes
- **Success**: Mensaje de éxito (ej. "Transacción completada").
- **Warning**: Mensaje de advertencia (ej. "Saldo bajo").
- **Error**: Mensaje de error (ej. "No se pudo procesar el pago").
- **Info**: Mensaje informativo (ej. "Actualización disponible").

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial del alerta.                                                  | Alerta visible en pantalla.             |
| Hover      | El cursor está sobre el alerta.                                             | Cambio de opacidad al pasar el cursor. |
| Dismissible | El alerta puede cerrarse por el usuario.                                    | Alerta con botón de cierre.            |

### Ejemplo de Uso
```yaml
# Ejemplo en una pantalla de pago
- type: Alert
  variant: Error
  message: "No se pudo procesar el pago. Intenta nuevamente."
  dismissible: true
  state: Default
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA para texto y fondo.
- **Foco**: Visible y claro si es interactivo.
- **Estructura**: Semántica correcta (`<alert>`, `<div role="alert">` o equivalente).
- **Redimensionamiento**: El texto se escala hasta 200%.

---

## 8. Modal

### Descripción
Componente que muestra contenido en una capa superpuesta, bloqueando la interacción con el resto de la pantalla.

### Variantes
- **Default**: Modal estándar con título, contenido y acciones.
- **Fullscreen**: Modal que ocupa toda la pantalla (ej. formulario largo).

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial del modal (oculto).                                          | Modal cerrado.                          |
| Open       | El modal está abierto.                                                      | Modal visible.                          |
| Hover      | El cursor está sobre un elemento interactivo del modal.                    | Cambio de color en botones.            |
| Focus      | Un elemento del modal está enfocado (navegación por teclado).              | Navegación con `Tab`.                  |

### Ejemplo de Uso
```yaml
# Ejemplo en una pantalla de perfil
- type: Modal
  variant: Default
  title: "Confirmar cambios"
  content: "¿Estás seguro de que deseas guardar estos cambios?"
  actions:
    - "Guardar"
    - "Cancelar"
  state: Open
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA para texto y bordes.
- **Foco**: El foco se maneja correctamente dentro del modal (no se escapa al fondo).
- **Estructura**: Semántica correcta (`<dialog>` o equivalente).
- **Cierre**: Opción para cerrar con `Esc` o botón.
- **Redimensionamiento**: El contenido se escala hasta 200%.

---

## 9. Tooltip

### Descripción
Componente que muestra información adicional cuando el usuario interactúa con un elemento (hover o focus).

### Variantes
- **Default**: Tooltip estándar con texto.
- **Rich**: Tooltip con contenido enriquecido (iconos, enlaces).

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial del tooltip (oculto).                                        | Tooltip no visible.                    |
| Hover      | El tooltip se muestra al pasar el cursor sobre el elemento.                | Tooltip con información adicional.     |
| Focus      | El tooltip se muestra al enfocar el elemento (navegación por teclado).     | Navegación con `Tab`.                  |

### Ejemplo de Uso
```yaml
# Ejemplo en un formulario
- type: Tooltip
  variant: Default
  target: "¿Qué es un CVU?"
  content: "El CVU es tu Clave Virtual Uniforme, necesaria para transferencias."
  state: Default
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA para texto y fondo.
- **Foco**: Visible y claro para navegación por teclado.
- **Tiempo**: El tooltip permanece visible el tiempo suficiente para ser leído.
- **Redimensionamiento**: El texto se escala hasta 200%.

---

## 10. Progress Bar

### Descripción
Componente que muestra el progreso de una operación o tarea.

### Variantes
- **Default**: Barra de progreso lineal.
- **Circular**: Barra de progreso circular (ej. carga de archivos).

### Estados
| Estado     | Descripción                                                                 | Ejemplo de Uso                          |
|------------|-----------------------------------------------------------------------------|-----------------------------------------|
| Default    | Estado inicial de la barra de progreso (0%).                               | Barra de progreso vacía.               |
| In Progress | La barra muestra el progreso actual.                                        | Progreso del 50%.                      |
| Complete   | La barra muestra el progreso completo (100%).                               | Progreso completado.                   |
| Error      | Indica que la operación falló.                                              | Progreso con mensaje de error.         |

### Ejemplo de Uso
```yaml
# Ejemplo en una pantalla de carga
- type: Progress Bar
  variant: Default
  value: 75
  max: 100
  state: In Progress
```

### Criterios de Accesibilidad
- **Contraste**: Cumple con WCAG 2.2 AA para la barra y el fondo.
- **Estructura**: Semántica correcta (`<progress>` o equivalente).
- **Etiqueta**: Asociada correctamente con `aria-label` o `label` visible.
- **Redimensionamiento**: La barra se escala hasta 200%.

---

## Referencias
- [Design Tokens (foundations/design-tokens.json)](../foundations/design-tokens.json)
- [Guías de Accesibilidad (foundations/accessibility-guidelines.md)](../foundations/accessibility-guidelines.md)
- [Material Design 3 Kit (Figma Community)](https://www.figma.com/community/file/1035203688168086460)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)

---

## Notas
- Esta especificación está sujeta a revisiones y actualizaciones basadas en feedback de usuarios y pruebas de usabilidad.
- Los componentes deben probarse en diferentes dispositivos y tamaños de pantalla para garantizar su correcto funcionamiento.