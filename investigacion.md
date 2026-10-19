# Investigación de Usuarios

Este documento recopila los hallazgos de la investigación realizada para fundamentar el diseño de la librería de componentes de la empresa fintech. La investigación incluyó entrevistas con usuarios, análisis de feedback existente y revisión de métricas de usabilidad.

## 1. Metodología

### Participantes
Se realizaron entrevistas con 12 usuarios de la plataforma fintech, divididos en tres grupos:
- **Usuarios frecuentes (6)**: Personas que utilizan la plataforma al menos 3 veces por semana para transferencias y pagos.
- **Usuarios ocasionales (4)**: Personas que utilizan la plataforma mensualmente para consultas de saldo y transacciones.
- **Nuevos usuarios (2)**: Personas que se registraron en la plataforma en los últimos 30 días.

### Técnicas
- **Entrevistas semiestructuradas**: Preguntas abiertas sobre experiencias previas, dificultades encontradas y sugerencias de mejora.
- **Análisis de métricas**: Revisión de datos de uso de la plataforma (tiempos de sesión, tasas de error, caminos de navegación).
- **Feedback existente**: Revisión de comentarios y tickets de soporte relacionados con la usabilidad de la interfaz.

## 2. Hallazgos

### Dificultades Reportadas

#### Usuarios Frecuentes
- **Inconsistencia en botones**: "A veces el botón de 'Confirmar' está en la parte inferior y otras veces en la superior. Me confunde." — Usuario 3, 34 años.
- **Falta de feedback visual**: "Cuando hago una transferencia, no siempre queda claro si se completó o no. A veces tengo que recargar la página." — Usuario 1, 28 años.
- **Estados de error poco claros**: "Los mensajes de error no me dicen qué hice mal. Solo aparece 'Error en la transacción' sin más detalles." — Usuario 5, 45 años.

#### Usuarios Ocasionales
- **Navegación confusa**: "No encuentro fácilmente el historial de transacciones. Siempre tengo que buscar en varios menús." — Usuario 7, 52 años.
- **Tamaño de texto pequeño**: "Los números de las cuentas y los montos son difíciles de leer. Tengo que hacer zoom para verlos bien." — Usuario 9, 60 años.
- **Falta de confirmación**: "No estoy seguro si mi pago se procesó correctamente. No hay un mensaje claro de éxito." — Usuario 8, 33 años.

#### Nuevos Usuarios
- **Dificultad para encontrar funciones básicas**: "No sabía dónde estaba la opción para hacer una transferencia. Tuve que buscar en Google." — Usuario 11, 25 años.
- **Sobrecarga de información**: "La pantalla de inicio tiene demasiada información. No sé por dónde empezar." — Usuario 12, 22 años.

### Sugerencias de Mejora

#### Usuarios Frecuentes
- **Botones más consistentes**: "Me gustaría que todos los botones importantes estén en el mismo lugar." — Usuario 2, 30 años.
- **Notificaciones más visibles**: "Quiero que las confirmaciones de transferencia sean más llamativas." — Usuario 4, 38 años.
- **Mensajes de error detallados**: "Que me digan exactamente qué hice mal y cómo corregirlo." — Usuario 6, 40 años.

#### Usuarios Ocasionales
- **Menús más intuitivos**: "Un menú más claro y organizado me ayudaría a encontrar lo que busco más rápido." — Usuario 10, 55 años.
- **Opción de ajustar tamaño de texto**: "Me gustaría poder aumentar el tamaño de la letra." — Usuario 9, 60 años.
- **Confirmaciones visuales**: "Un mensaje grande que diga 'Pago exitoso' me daría más seguridad." — Usuario 8, 33 años.

#### Nuevos Usuarios
- **Tutorial de inicio**: "Un breve tutorial al registrarme me ayudaría a entender cómo usar la plataforma." — Usuario 11, 25 años.
- **Interfaz más simple**: "Menos información en la pantalla de inicio, solo lo esencial." — Usuario 12, 22 años.

## 3. Análisis de Métricas

### Tiempos de Sesión
- **Usuarios frecuentes**: Promedio de 5 minutos por sesión.
- **Usuarios ocasionales**: Promedio de 3 minutos por sesión (principalmente consultas de saldo).
- **Nuevos usuarios**: Promedio de 8 minutos por sesión, con alta tasa de abandono en la primera interacción.

### Tasas de Error
- **Errores en transferencias**: 12% de las transferencias requieren más de un intento.
- **Errores en pagos**: 8% de los pagos fallan en el primer intento.
- **Errores de navegación**: 15% de los usuarios frecuentes y 30% de los usuarios ocasionales acceden a más de 3 pantallas antes de encontrar la función deseada.

### Caminos de Navegación
- **Transferencias**: El 60% de los usuarios frecuentes utilizan el menú lateral, mientras que el 40% lo hacen desde la pantalla de inicio.
- **Pagos**: El 70% de los usuarios ocasionales acceden a la función de pagos desde el menú superior.

## 4. Conclusiones

### Patrones Identificados
1. **Inconsistencia en la interfaz**: Los usuarios reportan confusión debido a la falta de consistencia en la ubicación de botones y menús.
2. **Falta de feedback visual**: Los usuarios no reciben suficiente confirmación de que sus acciones se completaron con éxito.
3. **Mensajes de error poco claros**: Los mensajes de error no proporcionan suficiente información para que los usuarios corrijan sus errores.
4. **Dificultad para nuevos usuarios**: La curva de aprendizaje es alta, especialmente para usuarios que no están familiarizados con plataformas fintech.

### Recomendaciones
1. **Librería de componentes consistente**: Crear una librería de componentes reutilizables con estados claros (hover, focus, error, loading) para garantizar consistencia en toda la interfaz.
2. **Notificaciones mejoradas**: Implementar notificaciones más visibles y detalladas para confirmar acciones exitosas y errores.
3. **Mensajes de error descriptivos**: Proporcionar mensajes de error que expliquen claramente el problema y cómo solucionarlo.
4. **Diseño accesible**: Asegurar que la interfaz cumpla con los criterios WCAG 2.2 para mejorar la legibilidad y usabilidad.
5. **Tutorial de inicio**: Incluir un tutorial breve para nuevos usuarios que explique las funciones básicas de la plataforma.

## 5. Próximos Pasos
- **Validar prototipos**: Crear prototipos de la nueva librería de componentes y probarlos con usuarios.
- **Iterar sobre feedback**: Recopilar feedback de los prototipos y ajustar el diseño según sea necesario.
- **Implementar en Figma**: Desarrollar los componentes en Figma con todas sus variantes y estados.
- **Documentar componentes**: Crear documentación detallada para cada componente, incluyendo ejemplos de uso y criterios de accesibilidad.