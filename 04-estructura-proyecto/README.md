# Estructura de un Proyecto Web

## 📁 ¿Cómo Organizar los Archivos?

Cuando creamos un sitio web, es importante mantener los archivos **organizados**. Aquí aprenderás la forma más común de estructurar un proyecto web.

## 🏗️ Estructura Básica

```
mi-proyecto/
│
├── index.html          (Página principal)
├── about.html          (Otras páginas HTML)
├── contact.html
│
├── css/
│   ├── style.css       (Estilos principales)
│   └── reset.css       (Reseteo de estilos)
│
├── js/
│   └── script.js       (JavaScript)
│
├── images/
│   ├── logo.png
│   ├── banner.jpg
│   └── foto-perfil.jpg
│
└── README.md           (Documentación del proyecto)
```

## 📄 El Archivo `index.html`

**`index.html`** es el nombre especial para la página principal. Los navegadores y servidores buscan este archivo por defecto.

Por ejemplo:
- `www.misitio.com` → muestra `index.html`
- `www.misitio.com/about.html` → muestra `about.html`

## 🎨 Carpeta CSS

Guarda todos tus archivos de estilos aquí:

```
css/
├── style.css        → Estilos principales
├── mobile.css       → Estilos para móviles (opcional)
└── components.css   → Estilos de componentes (opcional)
```

### Cómo enlazar CSS desde la carpeta:
```html
<link rel="stylesheet" href="css/style.css">
```

## 💻 Carpeta JS

Guarda todos tus archivos JavaScript aquí:

```
js/
├── script.js
└── utils.js
```

### Cómo enlazar JavaScript desde la carpeta:
```html
<script src="js/script.js"></script>
```

## 🖼️ Carpeta Images (o img)

Guarda todas las imágenes aquí organizadas por tipo o sección:

```
images/
├── logos/
│   └── logo.png
├── backgrounds/
│   └── hero-bg.jpg
└── products/
    ├── producto1.jpg
    └── producto2.jpg
```

### Cómo usar imágenes desde la carpeta:
```html
<img src="images/logo.png" alt="Logo">
<img src="images/products/producto1.jpg" alt="Producto 1">
```

## 📂 Rutas Relativas vs Absolutas

### Rutas Relativas (Recomendadas)
Rutas relativas a la ubicación del archivo actual:

```html
<!-- Desde index.html en la raíz -->
<link rel="stylesheet" href="css/style.css">
<img src="images/foto.jpg">

<!-- Desde about.html en la raíz -->
<link rel="stylesheet" href="css/style.css">

<!-- Desde un archivo en carpeta /pages/ -->
<link rel="stylesheet" href="../css/style.css">  <!-- ../ sube un nivel -->
```

### Rutas Absolutas
Incluyen la ruta completa desde la raíz del servidor:

```html
<link rel="stylesheet" href="/css/style.css">
<img src="/images/foto.jpg">
```

## 🎯 Plantilla de Proyecto Básico

Aquí está la estructura mínima recomendada para empezar:

**index.html:**
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Sitio Web</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Bienvenido a Mi Sitio</h1>
    </header>
    
    <main>
        <p>Contenido principal aquí</p>
    </main>
    
    <footer>
        <p>&copy; 2024 Mi Sitio Web</p>
    </footer>
    
    <script src="js/script.js"></script>
</body>
</html>
```

**css/style.css:**
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
    min-height: 70vh;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
}
```

## ✨ Buenas Prácticas

1. **Nombres de archivos:**
   - Usa minúsculas: `style.css` no `Style.css`
   - Usa guiones en vez de espacios: `mi-pagina.html` no `mi pagina.html`
   - Sé descriptivo: `about.html` no `pagina2.html`

2. **Organización:**
   - Un archivo CSS por carpeta (al principio)
   - Separa las imágenes por categoría si tienes muchas
   - Mantén una estructura consistente

3. **Comentarios:**
   - Comenta tu código CSS con `/* comentario */`
   - Comenta tu HTML con `<!-- comentario -->`

4. **Etiquetas semánticas en HTML:**
   - Usa `<header>`, `<nav>`, `<main>`, `<footer>` en vez de solo `<div>`
   - Ayuda a la accesibilidad y SEO

## 🎯 Próximo Paso

En la carpeta encontrarás una plantilla lista para usar. Cópiala y experimenta creando tu propio proyecto.
