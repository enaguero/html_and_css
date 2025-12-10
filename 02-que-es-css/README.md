# ¿Qué es CSS?

## 📖 Definición

**CSS** significa **C**ascading **S**tyle **S**heets (Hojas de Estilo en Cascada).

Es el lenguaje que se usa para **diseñar y dar estilo** a las páginas web. Si HTML es el esqueleto, CSS es la **piel, ropa y maquillaje** de la página web.

## 🎨 ¿Para qué sirve?

CSS sirve para controlar:
- **Colores** (texto, fondos, bordes)
- **Tamaños** (fuentes, elementos)
- **Espaciados** (márgenes, rellenos)
- **Posiciones** (dónde se ubican los elementos)
- **Animaciones** y efectos visuales
- **Diseño responsive** (adaptarse a diferentes pantallas)

## 🧱 ¿Cómo funciona?

CSS usa **reglas** que siguen esta estructura:

```css
selector {
    propiedad: valor;
}
```

### Ejemplo:
```css
p {
    color: blue;
    font-size: 18px;
}
```

Esto significa: "Todos los párrafos (`<p>`) tendrán texto azul y tamaño de fuente de 18 píxeles".

## 🎯 Selectores Básicos

Los selectores indican **qué elementos** queremos estilizar:

| Selector | Sintaxis | Ejemplo | Descripción |
|----------|----------|---------|-------------|
| **Etiqueta** | `etiqueta` | `p { }` | Selecciona todas las etiquetas `<p>` |
| **Clase** | `.nombre` | `.destacado { }` | Selecciona elementos con `class="destacado"` |
| **ID** | `#nombre` | `#titulo { }` | Selecciona el elemento con `id="titulo"` |
| **Universal** | `*` | `* { }` | Selecciona todos los elementos |

### Ejemplos:

```css
/* Por etiqueta */
h1 {
    color: red;
}

/* Por clase */
.importante {
    font-weight: bold;
}

/* Por ID */
#encabezado {
    background-color: yellow;
}
```

## 📌 ¿Cómo Conectar CSS con HTML?

Hay 3 formas de aplicar CSS:

### 1. CSS Externo (Recomendado)
Crear un archivo `.css` separado y enlazarlo:

**HTML:**
```html
<head>
    <link rel="stylesheet" href="estilos.css">
</head>
```

**estilos.css:**
```css
body {
    background-color: lightblue;
}
```

### 2. CSS Interno
Escribir CSS dentro del `<head>`:

```html
<head>
    <style>
        body {
            background-color: lightblue;
        }
    </style>
</head>
```

### 3. CSS en Línea (No recomendado)
Aplicar estilos directamente en la etiqueta:

```html
<p style="color: red;">Texto rojo</p>
```

## 🎨 Propiedades Más Comunes

### Colores
```css
color: blue;              /* Color del texto */
background-color: yellow; /* Color de fondo */
```

### Tipografía
```css
font-size: 20px;          /* Tamaño de letra */
font-family: Arial;       /* Tipo de letra */
font-weight: bold;        /* Grosor (negrita) */
text-align: center;       /* Alineación del texto */
```

### Tamaños
```css
width: 200px;             /* Ancho */
height: 100px;            /* Alto */
```

### Espaciados (¡Importante!)
```css
margin: 20px;             /* Espacio exterior */
padding: 10px;            /* Espacio interior */
border: 2px solid black;  /* Borde */
```

## 🎯 Valores Comunes

| Unidad | Significado | Ejemplo |
|--------|-------------|---------|
| `px` | Píxeles (fijo) | `font-size: 16px;` |
| `%` | Porcentaje (relativo al padre) | `width: 50%;` |
| `em` | Relativo al tamaño de fuente | `padding: 1em;` |
| `rem` | Relativo al tamaño de fuente raíz | `font-size: 1.5rem;` |

## ✨ Importante Recordar

1. CSS controla el **aspecto visual**, no la estructura
2. Los estilos se pueden **heredar** de elementos padre a hijo
3. Si hay conflictos, el CSS más **específico** gana
4. El orden importa: lo último que se lee tiene prioridad (por eso se llama "en cascada")

## 🎯 Próximo Paso

Abre `ejercicio.html` para practicar aplicando estilos CSS.
