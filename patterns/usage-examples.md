# Patrones de Uso para Componentes

Este documento describe cómo combinar los componentes definidos en la librería para crear patrones de interfaz comunes. Los ejemplos incluyen capturas de pantalla (simuladas con descripciones) y código en formato Figma.

## 1. Tarjeta de Producto (Product Card)
**Descripción:** Tarjeta utilizada para mostrar productos en un catálogo o resultados de búsqueda.

**Componentes utilizados:**
- Card (Default)
- Image (Componente base)
- Text (Título y descripción)
- Button (Primary Action)
- Icon (Opcional)

**Estructura:**
```
Frame (Product Card)
  Width: 320
  Height: Auto
  Layout: Vertical
  Padding: 0
  Fill: #FFFFFF
  Stroke: 1 solid #E0E0E0
  Corner Radius: 12
  
  Image (Product Image)
    Width: Fill container
    Height: 180
    Scale Mode: Fill
    
  Frame (Content)
    Width: Fill container
    Height: Auto
    Padding: 16
    Layout: Vertical
    
    Text (Product Title)
      Value: "Product Name"
      Font: Inter SemiBold 16
      Fill: #1A1A1A
      
    Text (Product Description)
      Value: "Brief description of the product."
      Font: Inter Regular 14
      Fill: #333333
      Line Height: 20
      
    Frame (Price and Action)
      Width: Fill container
      Height: Auto
      Layout: Horizontal
      Padding: 8 0 0 0
      
      Text (Price)
        Value: "$99.99"
        Font: Inter Bold 16
        Fill: #1A1A1A
        
      Spacer
        Width: Fill container
        
      Button (Primary Action)
        Variant: Primary
        Text: "Add to Cart"
        Width: Auto
        Height: 36
```

**Estados:**
- **Default:** Muestra la información del producto y el botón de acción.
- **Hover:** Destaca la tarjeta con una sombra sutil y cambia el estilo del botón.
- **Focus:** Resalta el contorno de la tarjeta para navegación con teclado.
- **Disabled:** Desactiva la tarjeta si el producto no está disponible.

**Criterios de Accesibilidad:**
- Asegurar que el contraste de color cumple con WCAG 2.2 (mínimo 4.5:1 para texto normal).
- Proporcionar texto alternativo para la imagen del producto.
- Permitir la navegación con teclado y resaltar el estado de enfoque.

---

## 2. Formulario con Validación
**Descripción:** Formulario que incluye campos de entrada, validación en tiempo real y retroalimentación visual.

**Componentes utilizados:**
- Card (Default)
- Input (Text, Email, Password)
- Button (Primary Action)
- Text (Labels y mensajes de error)
- Icon (Opcional, para indicar errores)

**Estructura:**
```
Frame (Form Card)
  Width: 400
  Height: Auto
  Layout: Vertical
  Padding: 0
  Fill: #FFFFFF
  Stroke: 1 solid #E0E0E0
  Corner Radius: 12
  
  Frame (Header)
    Width: Fill container
    Height: Auto
    Padding: 16
    
    Text (Form Title)
      Value: "Sign Up"
      Font: Inter SemiBold 18
      Fill: #1A1A1A
      
  Frame (Form Fields)
    Width: Fill container
    Height: Auto
    Padding: 16
    Layout: Vertical
    
    Frame (Input Group: Name)
      Width: Fill container
      Height: Auto
      Layout: Vertical
      Spacing: 4
      
      Text (Label)
        Value: "Full Name"
        Font: Inter Regular 14
        Fill: #333333
        
      Input (Text)
        Variant: Default
        Placeholder: "Enter your full name"
        Width: Fill container
        Height: 40
        
      Text (Error Message)
        Value: "Name is required"
        Font: Inter Regular 12
        Fill: #F44336
        Visible: False
        
    Frame (Input Group: Email)
      Width: Fill container
      Height: Auto
      Layout: Vertical
      Spacing: 4
      
      Text (Label)
        Value: "Email"
        Font: Inter Regular 14
        Fill: #333333
        
      Input (Email)
        Variant: Default
        Placeholder: "Enter your email"
        Width: Fill container
        Height: 40
        
      Text (Error Message)
        Value: "Please enter a valid email"
        Font: Inter Regular 12
        Fill: #F44336
        Visible: False
        
    Frame (Input Group: Password)
      Width: Fill container
      Height: Auto
      Layout: Vertical
      Spacing: 4
      
      Text (Label)
        Value: "Password"
        Font: Inter Regular 14
        Fill: #333333
        
      Input (Password)
        Variant: Default
        Placeholder: "Create a password"
        Width: Fill container
        Height: 40
        
      Text (Error Message)
        Value: "Password must be at least 8 characters"
        Font: Inter Regular 12
        Fill: #F44336
        Visible: False
        
  Frame (Footer)
    Width: Fill container
    Height: Auto
    Padding: 16
    Layout: Horizontal
    
    Button (Primary Action)
      Variant: Primary
      Text: "Submit"
      Width: Fill container
      Height: 40
```

**Estados:**
- **Default:** Campos vacíos, botón activo.
- **Focus:** Campo resaltado para entrada de datos.
- **Error:** Campo con error muestra mensaje y borde rojo.
- **Loading:** Botón muestra spinner durante el envío del formulario.

**Criterios de Accesibilidad:**
- Asociar etiquetas con campos de entrada usando `for` y `id`.
- Proporcionar mensajes de error claros y específicos.
- Asegurar que los campos de entrada son accesibles mediante teclado.
- Validar el contraste de color para los mensajes de error.

---

## 3. Panel de Control (Dashboard)
**Descripción:** Panel de control que muestra métricas clave y acciones rápidas.

**Componentes utilizados:**
- Card (Default)
- Text (Títulos y valores)
- Button (Primary y Secondary Actions)
- Icon (Opcional, para acciones rápidas)

**Estructura:**
```
Frame (Dashboard)
  Width: 1200
  Height: Auto
  Layout: Vertical
  Padding: 24
  Fill: #F5F5F5
  
  Frame (Header)
    Width: Fill container
    Height: Auto
    Layout: Horizontal
    Padding: 0 0 24 0
    
    Text (Title)
      Value: "Dashboard"
      Font: Inter SemiBold 24
      Fill: #1A1A1A
      
    Spacer
      Width: Fill container
      
    Button (Primary Action)
      Variant: Primary
      Text: "New Action"
      Width: Auto
      Height: 40
      
  Frame (Metrics)
    Width: Fill container
    Height: Auto
    Layout: Horizontal
    Spacing: 24
    Padding: 24 0 0 0
    
    Card (Metric Card)
      Width: 280
      Height: 120
      Layout: Vertical
      Padding: 16
      
      Text (Label)
        Value: "Total Users"
        Font: Inter Regular 14
        Fill: #666666
        
      Text (Value)
        Value: "1,234"
        Font: Inter Bold 24
        Fill: #1A1A1A
        
    Card (Metric Card)
      Width: 280
      Height: 120
      Layout: Vertical
      Padding: 16
      
      Text (Label)
        Value: "Active Sessions"
        Font: Inter Regular 14
        Fill: #666666
        
      Text (Value)
        Value: "567"
        Font: Inter Bold 24
        Fill: #1A1A1A
        
    Card (Metric Card)
      Width: 280
      Height: 120
      Layout: Vertical
      Padding: 16
      
      Text (Label)
        Value: "Revenue"
        Font: Inter Regular 14
        Fill: #666666
        
      Text (Value)
        Value: "$12,345"
        Font: Inter Bold 24
        Fill: #2E7D32
        
  Frame (Quick Actions)
    Width: Fill container
    Height: Auto
    Layout: Horizontal
    Spacing: 16
    Padding: 24 0 0 0
    
    Card (Action Card)
      Width: 200
      Height: 100
      Layout: Vertical
      Padding: 16
      
      Icon (Action Icon)
        Name: add
        Size: 24
        Color: #2196F3
        
      Text (Action Label)
        Value: "Add User"
        Font: Inter SemiBold 14
        Fill: #1A1A1A
        
    Card (Action Card)
      Width: 200
      Height: 100
      Layout: Vertical
      Padding: 16
      
      Icon (Action Icon)
        Name: edit
        Size: 24
        Color: #FF9800
        
      Text (Action Label)
        Value: "Edit Profile"
        Font: Inter SemiBold 14
        Fill: #1A1A1A
        
    Card (Action Card)
      Width: 200
      Height: 100
      Layout: Vertical
      Padding: 16
      
      Icon (Action Icon)
        Name: delete
        Size: 24
        Color: #F44336
        
      Text (Action Label)
        Value: "Delete Item"
        Font: Inter SemiBold 14
        Fill: #1A1A1A
```

**Estados:**
- **Default:** Muestra métricas y acciones rápidas.
- **Hover:** Resalta la tarjeta de acción al pasar el cursor.
- **Focus:** Resalta la tarjeta de acción para navegación con teclado.

**Criterios de Accesibilidad:**
- Asegurar que el contraste de color cumple con WCAG 2.2.
- Proporcionar texto alternativo para los íconos.
- Permitir la navegación con teclado.

---

## 4. Modal de Confirmación
**Descripción:** Modal utilizado para confirmar acciones críticas o mostrar información importante.

**Componentes utilizados:**
- Card (Default)
- Text (Título y mensaje)
- Button (Primary y Secondary Actions)
- Overlay (Componente base)

**Estructura:**
```
Frame (Modal)
  Width: 400
  Height: Auto
  Layout: Vertical
  Padding: 0
  Fill: #FFFFFF
  Stroke: 1 solid #E0E0E0
  Corner Radius: 12
  
  Frame (Header)
    Width: Fill container
    Height: Auto
    Padding: 24 24 16 24
    
    Text (Title)
      Value: "Confirm Action"
      Font: Inter SemiBold 18
      Fill: #1A1A1A
      
  Frame (Content)
    Width: Fill container
    Height: Auto
    Padding: 0 24 24 24
    
    Text (Message)
      Value: "Are you sure you want to delete this item? This action cannot be undone."
      Font: Inter Regular 14
      Fill: #333333
      Line Height: 20
      
  Frame (Footer)
    Width: Fill container
    Height: Auto
    Layout: Horizontal
    Padding: 16 24 24 24
    Spacing: 16
    
    Button (Secondary Action)
      Variant: Secondary
      Text: "Cancel"
      Width: Auto
      Height: 40
      
    Button (Primary Action)
      Variant: Primary
      Text: "Confirm"
      Width: Auto
      Height: 40
```

**Estados:**
- **Default:** Modal centrado con overlay semitransparente.
- **Hover:** Botones cambian de estilo al pasar el cursor.
- **Focus:** Botones resaltados para navegación con teclado.

**Criterios de Accesibilidad:**
- Asegurar que el modal es accesible mediante teclado (foco en el primer elemento interactivo).
- Proporcionar una forma clara de cerrar el modal (ej., botón de cancelar o tecla Escape).
- Validar el contraste de color para el texto y los botones.