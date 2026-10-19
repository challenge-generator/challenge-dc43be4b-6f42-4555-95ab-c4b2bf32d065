# Especificación de Componentes

Esta especificación detalla los componentes reutilizables para la librería de diseño de la empresa fintech. Cada componente incluye su descripción, variantes de estado, ejemplos de uso y criterios de accesibilidad según WCAG 2.2.

## 1. Botón (Button)

### Descripción
Componente interactivo que permite al usuario realizar acciones como enviar formularios, navegar entre pantallas o confirmar operaciones.

### Estados
| Estado      | Descripción                                                                 | Token de Color (Background) | Token de Color (Texto) | Token de Borde       |
|-------------|-----------------------------------------------------------------------------|-----------------------------|------------------------|-------------------------|
| Default     | Estado inicial del botón.                                                  | `--color-primary-500`       | `--color-white`        | `--color-primary-500` |
| Hover       | Estado cuando el usuario pasa el cursor sobre el botón.                   | `--color-primary-600`       | `--color-white`        | `--color-primary-600` |
| Focus       | Estado cuando el botón está seleccionado mediante teclado (ej. Tab).      | `--color-primary-500`       | `--color-white`        | `--color-focus`       |
| Disabled    | Estado cuando el botón no está disponible para interacción.                | `--color-gray-200`          | `--color-gray-500`     | `--color-gray-200`    |
| Error       | Estado cuando el botón está asociado a un error (ej. envío fallido).      | `--color-error-500`         | `--color-white`        | `--color-error-500`   |
| Loading     | Estado cuando el botón está procesando una acción (ej. envío de formulario). | `--color-primary-500`       | `--color-white`        | `--color-primary-500` |

### Ejemplo de Uso
- **Acción primaria**: Confirmar transferencia bancaria.
- **Acción secundaria**: Cancelar operación.

### Criterios de Accesibilidad
- **Contraste**: Relación de contraste mínima de 4.5:1 para texto y bordes.
- **Foco**: Borde visible de al menos 2px con color `--color-focus`.
- **Orden de lectura**: Botones deben seguir el flujo lógico de la interfaz.
- **Alternativas textuales**: Iconos dentro de botones deben tener `aria-label` o texto alternativo.

---

## 2. Campo de Entrada (Input)

### Descripción
Componente para ingresar datos textuales o numéricos, como nombres, contraseñas o montos.

### Estados
| Estado      | Descripción                                                                 | Token de Color (Background) | Token de Color (Texto) | Token de Borde       |
|-------------|-----------------------------------------------------------------------------|-----------------------------|------------------------|-------------------------|
| Default     | Estado inicial del campo.                                                   | `--color-white`             | `--color-gray-900`     | `--color-gray-300`     |
| Hover       | Estado cuando el usuario pasa el cursor sobre el campo.                    | `--color-white`             | `--color-gray-900`     | `--color-gray-500`     |
| Focus       | Estado cuando el campo está seleccionado.                                   | `--color-white`             | `--color-gray-900`     | `--color-primary-500` |
| Disabled    | Estado cuando el campo no está disponible para interacción.                | `--color-gray-100`          | `--color-gray-500`     | `--color-gray-200`    |
| Error       | Estado cuando el campo contiene un error (ej. formato inválido).          | `--color-white`             | `--color-error-500`    | `--color-error-500`   |
| Loading     | Estado cuando el campo está procesando datos (ej. validación en tiempo real). | `--color-white`             | `--color-gray-900`     | `--color-gray-300`     |

### Ejemplo de Uso
- **Entrada de texto**: Nombre completo.
- **Entrada numérica**: Monto de transferencia.
- **Entrada de contraseña**: Campo con enmascaramiento.

### Criterios de Accesibilidad
- **Contraste**: Relación de contraste mínima de 4.5:1 para texto y bordes.
- **Foco**: Borde visible de al menos 2px con color `--color-primary-500`.
- **Etiquetas**: Cada campo debe tener una etiqueta asociada (`<label>` o `aria-label`).
- **Feedback de error**: Mensaje descriptivo visible y accesible para lectores de pantalla.

---

## 3. Tarjeta (Card)

### Descripción
Componente contenedor para agrupar información relacionada, como detalles de una cuenta bancaria o resumen de transacciones.

### Estados
| Estado      | Descripción                                                                 | Token de Color (Background) | Token de Color (Texto) | Token de Borde       |
|-------------|-----------------------------------------------------------------------------|-----------------------------|------------------------|-------------------------|
| Default     | Estado inicial de la tarjeta.                                               | `--color-white`             | `--color-gray-900`     | `--color-gray-200`    |
| Hover       | Estado cuando el usuario pasa el cursor sobre la tarjeta.                  | `--color-gray-50`           | `--color-gray-900`     | `--color-gray-300`    |
| Focus       | Estado cuando la tarjeta está seleccionada mediante teclado.                | `--color-white`             | `--color-gray-900`     | `--color-focus`       |
| Disabled    | Estado cuando la tarjeta no está disponible para interacción.              | `--color-gray-100`          | `--color-gray-500`     | `--color-gray-200`    |
| Error       | Estado cuando la tarjeta contiene información errónea.                     | `--color-white`             | `--color-error-500`    | `--color-error-500`   |

### Ejemplo de Uso
- **Tarjeta de cuenta**: Muestra saldo disponible y últimas transacciones.
- **Tarjeta de transacción**: Detalles de una transferencia reciente.

### Criterios de Accesibilidad
- **Contraste**: Relación de contraste mínima de 4.5:1 para texto y bordes.
- **Foco**: Borde visible de al menos 2px con color `--color-focus`.
- **Orden de lectura**: La información debe seguir un flujo lógico y accesible.
- **Alternativas textuales**: Imágenes o iconos dentro de la tarjeta deben tener `aria-label`.

---

## 4. Notificación (Notification)

### Descripción
Componente para mostrar mensajes temporales al usuario, como confirmaciones o alertas.

### Estados
| Estado      | Descripción                                                                 | Token de Color (Background) | Token de Color (Texto) |
|-------------|-----------------------------------------------------------------------------|-----------------------------|------------------------|
| Success     | Notificación de éxito (ej. transferencia completada).                     | `--color-success-100`       | `--color-success-800`  |
| Warning     | Notificación de advertencia (ej. saldo bajo).                              | `--color-warning-100`       | `--color-warning-800`  |
| Error       | Notificación de error (ej. fallo en la transacción).                       | `--color-error-100`         | `--color-error-800`    |
| Info        | Notificación informativa (ej. actualización disponible).                   | `--color-info-100`          | `--color-info-800`     |

### Ejemplo de Uso
- **Éxito**: "Transferencia completada con éxito."
- **Advertencia**: "Saldo insuficiente para esta operación."
- **Error**: "Fallo en la conexión. Inténtelo más tarde."

### Criterios de Accesibilidad
- **Contraste**: Relación de contraste mínima de 4.5:1 para texto.
- **Duración**: Notificaciones deben permanecer visibles el tiempo suficiente para ser leídas.
- **Alternativas textuales**: Mensajes deben ser accesibles para lectores de pantalla.

---

## 5. Tablas (Table)

### Descripción
Componente para mostrar datos tabulares, como historial de transacciones o detalles de cuentas.

### Estados
| Estado      | Descripción                                                                 | Token de Color (Fondo de fila) | Token de Color (Texto) |
|-------------|-----------------------------------------------------------------------------|-------------------------------|------------------------|
| Default     | Estado inicial de la tabla.                                                 | `--color-white`               | `--color-gray-900`     |
| Hover       | Estado cuando el usuario pasa el cursor sobre una fila.                    | `--color-gray-50`             | `--color-gray-900`     |
| Selected    | Estado cuando una fila está seleccionada.                                   | `--color-primary-50`          | `--color-primary-900`  |

### Ejemplo de Uso
- **Historial de transacciones**: Muestra fecha, concepto y monto.
- **Detalles de cuentas**: Muestra número de cuenta, tipo y saldo.

### Criterios de Accesibilidad
- **Contraste**: Relación de contraste mínima de 4.5:1 para texto y filas.
- **Orden de lectura**: Las celdas deben estar asociadas a sus encabezados.
- **Alternativas textuales**: Datos numéricos o iconos deben tener descripciones accesibles.

---

## Convenciones de Documentación
- **Descripción**: Explica el propósito del componente y su uso típico.
- **Estados**: Detalla todos los estados posibles del componente con sus tokens de diseño.
- **Ejemplo de Uso**: Proporciona ejemplos concretos de cómo se utiliza el componente.
- **Criterios de Accesibilidad**: Lista los requisitos de accesibilidad según WCAG 2.2.