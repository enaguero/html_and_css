# El Box Model (Modelo de Caja)

## 📦 ¿Qué es el Box Model?

Todos los elementos HTML son **cajas rectangulares**. El Box Model es cómo CSS describe el espacio que ocupa cada elemento.

Imagina que cada elemento es una **caja de regalo**:
- El **contenido** es el regalo dentro
- El **padding** es el papel protector alrededor del regalo
- El **border** es la caja misma
- El **margin** es el espacio entre esta caja y otras cajas

## 🎨 Partes del Box Model

```
┌─────────────── MARGIN ────────────────┐
│  ┌────────── BORDER ──────────────┐  │
│  │  ┌─────── PADDING ──────────┐  │  │
│  │  │                           │  │  │
│  │  │       CONTENIDO          │  │  │
│  │  │      (width x height)    │  │  │
│  │  │                           │  │  │
│  │  └───────────────────────────┘  │  │
│  └──────────────────────────────────┘  │
└────────────────────────────────────────┘
```

### 1. **CONTENIDO** (Content)
Es el espacio donde va el texto, imágenes, o cualquier contenido del elemento.

```css
.caja {
    width: 200px;     /* Ancho del contenido */
    height: 100px;    /* Alto del contenido */
}
```

### 2. **PADDING** (Relleno)
Es el **espacio interior** entre el contenido y el borde.

- Empuja el contenido hacia dentro
- Hace que la caja se vea más grande
- Tiene el mismo color de fondo que el elemento

```css
.caja {
    padding: 20px;    /* 20px de espacio interno en todos los lados */
}
```

### 3. **BORDER** (Borde)
Es el **borde** que rodea el padding y el contenido.

```css
.caja {
    border: 2px solid black;  /* Grosor, estilo, color */
}
```

### 4. **MARGIN** (Margen)
Es el **espacio exterior** que separa el elemento de otros elementos.

- Crea separación entre elementos
- Es transparente (no tiene color)
- Empuja a otros elementos

```css
.caja {
    margin: 15px;     /* 15px de espacio externo en todos los lados */
}
```

## 🔍 PADDING vs MARGIN - La Diferencia Clave

Esta es la confusión más común. Aquí está la diferencia:

### PADDING (Interior)
- Espacio **DENTRO** del elemento
- Entre el contenido y el borde
- Tiene el color de fondo del elemento
- Hace que el elemento sea más grande

```css
.con-padding {
    background-color: lightblue;
    padding: 30px;
    /* El fondo azul incluye el padding */
}
```

### MARGIN (Exterior)
- Espacio **FUERA** del elemento
- Separa el elemento de otros elementos
- Es transparente
- No afecta el tamaño del elemento mismo

```css
.con-margin {
    background-color: lightblue;
    margin: 30px;
    /* El fondo azul NO incluye el margin */
}
```

## 📐 WIDTH y HEIGHT

### Width (Ancho)
Define el ancho del **contenido** del elemento.

```css
.caja {
    width: 300px;      /* Ancho fijo */
    width: 50%;        /* 50% del elemento padre */
    width: auto;       /* Automático (por defecto) */
    max-width: 500px;  /* Ancho máximo */
    min-width: 200px;  /* Ancho mínimo */
}
```

### Height (Alto)
Define el alto del **contenido** del elemento.

```css
.caja {
    height: 200px;     /* Alto fijo */
    height: 50vh;      /* 50% de la altura de la ventana */
    height: auto;      /* Automático según contenido */
    max-height: 400px; /* Alto máximo */
    min-height: 100px; /* Alto mínimo */
}
```

## 🎯 Formas de Aplicar Padding y Margin

### 1. Todos los lados iguales
```css
padding: 20px;     /* 20px en todos los lados */
margin: 10px;      /* 10px en todos los lados */
```

### 2. Vertical y Horizontal
```css
padding: 20px 40px;   /* 20px arriba/abajo, 40px izq/der */
margin: 10px 30px;    /* 10px arriba/abajo, 30px izq/der */
```

### 3. Top, Horizontal, Bottom
```css
padding: 10px 20px 30px;   /* 10px arriba, 20px lados, 30px abajo */
```

### 4. Cuatro lados (sentido horario)
```css
padding: 10px 20px 30px 40px;  /* arriba, derecha, abajo, izquierda */
margin: 5px 10px 15px 20px;
```

### 5. Lados individuales
```css
padding-top: 10px;
padding-right: 20px;
padding-bottom: 30px;
padding-left: 40px;

margin-top: 5px;
margin-right: 10px;
margin-bottom: 15px;
margin-left: 20px;
```

## 📊 Cálculo del Tamaño Total

### Sin `box-sizing`
```css
.caja {
    width: 200px;
    padding: 20px;
    border: 5px;
    margin: 10px;
}
/* Ancho total = 200 + 20 + 20 + 5 + 5 = 250px (sin contar margin) */
```

### Con `box-sizing: border-box` (Recomendado)
```css
* {
    box-sizing: border-box;
}

.caja {
    width: 200px;
    padding: 20px;
    border: 5px;
}
/* Ancho total = 200px (padding y border están incluidos) */
```

## 💡 Trucos Útiles

### Centrar un elemento horizontalmente
```css
.centrado {
    width: 500px;
    margin: 0 auto;   /* 0 arriba/abajo, auto izq/der */
}
```

### Resetear estilos
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

### Espaciado consistente
```css
section {
    padding: 40px 20px;     /* Más espacio vertical */
    margin-bottom: 30px;     /* Separación entre secciones */
}
```

## ⚠️ Errores Comunes

1. **Confundir padding con margin**
   - ¿Quieres más espacio dentro? → `padding`
   - ¿Quieres separar de otros elementos? → `margin`

2. **Olvidar box-sizing**
   - Sin esto, width no incluye padding y border
   - Siempre usa: `box-sizing: border-box;`

3. **Usar width: 100% con padding**
   - Puede causar desbordamiento
   - Solución: usa `box-sizing: border-box;`

## 🎯 Próximo Paso

Abre `ejercicio-box-model.html` para practicar con ejemplos visuales interactivos.
