# Proyecto Final: Calculadora

## 🎯 Objetivo

Crear una calculadora **visual** usando HTML y CSS. Esta calculadora será solo la interfaz (sin funcionalidad de cálculo).

Este proyecto combina todos los conceptos aprendidos:
- Estructura HTML
- Box Model (padding, margin, width)
- Flexbox para el layout
- Estilos CSS (colores, bordes, efectos)

## 📋 Características del Proyecto

### Lo que incluye:
- Pantalla de la calculadora
- Botones numéricos (0-9)
- Botones de operaciones (+, -, ×, ÷)
- Botón de igual (=)
- Botón de borrar (C)
- Diseño responsive y moderno
- Efectos hover en los botones

### Lo que NO incluye (por ahora):
- Funcionalidad JavaScript
- Cálculos reales

## 🏗️ Estructura

La calculadora se divide en:

1. **Contenedor Principal** - La caja de la calculadora
2. **Pantalla** - Donde se mostrarían los números
3. **Grid de Botones** - Layout con Flexbox o CSS Grid
4. **Botones** - Números y operaciones

## 🎨 Conceptos CSS Aplicados

### Box Model
```css
.boton {
    width: 70px;
    height: 70px;
    padding: 20px;
    margin: 5px;
}
```

### Flexbox
```css
.calculadora {
    display: flex;
    flex-direction: column;
}

.fila-botones {
    display: flex;
    gap: 10px;
}
```

### Position (para alineación)
```css
.calculadora {
    position: relative;
    margin: 50px auto; /* Centrar */
}
```

## 💡 Desafíos del Proyecto

1. **Layout de la calculadora** - Usar Flexbox para organizar los botones
2. **Diseño de botones** - Hacer botones atractivos y clickeables
3. **Espaciado correcto** - Aplicar margin y padding apropiados
4. **Colores diferentes** - Distinguir números de operaciones
5. **Responsive** - Que se vea bien en diferentes tamaños

## 🎯 Paso a Paso

### Paso 1: Estructura HTML
Crear la estructura básica con:
- Contenedor de la calculadora
- Pantalla
- Botones organizados en filas

### Paso 2: Estilos Básicos
- Dar forma al contenedor
- Estilizar la pantalla
- Estilizar los botones

### Paso 3: Layout con Flexbox
- Organizar botones en filas
- Usar gap para espaciado
- Alinear elementos

### Paso 4: Detalles y Efectos
- Colores diferenciados
- Efectos hover
- Sombras y bordes

### Paso 5: Refinamiento
- Ajustar tamaños
- Mejorar espaciado
- Centrar en la página

## 🎨 Sugerencias de Diseño

### Paleta de Colores (ejemplo):
- Fondo calculadora: `#2c3e50`
- Pantalla: `#34495e`
- Botones números: `#ecf0f1`
- Botones operaciones: `#3498db`
- Botón igual: `#27ae60`
- Botón borrar: `#e74c3c`

### Tipografía:
- Fuente: `Arial, sans-serif` o `'Segoe UI'`
- Tamaño pantalla: `32px` o mayor
- Tamaño botones: `20px`

## 🎯 Próximo Paso

Abre `calculadora.html` para ver el proyecto completo comentado y listo para personalizar.

## 🚀 Retos Adicionales (Opcional)

Una vez terminada la calculadora básica, puedes intentar:

1. **Cambiar el diseño** - Diferentes colores y formas
2. **Agregar más botones** - Paréntesis, porcentaje, etc.
3. **Hacer responsive** - Que se adapte a móviles
4. **Crear una variante** - Calculadora científica (solo visual)
5. **Agregar JavaScript** - Hacer que funcione realmente (¡desafío avanzado!)

## ✨ Importante

Este proyecto es la culminación de lo aprendido. Tómate tu tiempo para:
- Entender cada línea de CSS
- Experimentar con valores
- Personalizar a tu gusto
- Practicar el Box Model y Flexbox

¡Disfruta creando tu calculadora! 🎉
