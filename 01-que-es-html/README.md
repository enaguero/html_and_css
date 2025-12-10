# ¿Qué es HTML?

## 📖 Definición

**HTML** significa **H**yper**T**ext **M**arkup **L**anguage (Lenguaje de Marcado de Hipertexto).

Es el lenguaje que se usa para **estructurar** el contenido de las páginas web. Piensa en HTML como el **esqueleto** de una página web.

## 🏗️ ¿Para qué sirve?

HTML sirve para definir:
- **Títulos** y subtítulos
- **Párrafos** de texto
- **Imágenes**
- **Enlaces** (links)
- **Listas**
- **Formularios**
- Y mucho más...

## 🧱 ¿Cómo funciona?

HTML usa **etiquetas** (tags) para marcar el contenido. Las etiquetas van entre corchetes angulares `< >`.

La mayoría de etiquetas tienen:
- Una **etiqueta de apertura**: `<etiqueta>`
- El **contenido**
- Una **etiqueta de cierre**: `</etiqueta>`

### Ejemplo básico:
```html
<p>Este es un párrafo</p>
```

## 📝 Etiquetas Más Comunes

| Etiqueta | Descripción | Ejemplo |
|----------|-------------|---------|
| `<h1>` hasta `<h6>` | Títulos (h1 es el más grande) | `<h1>Título Principal</h1>` |
| `<p>` | Párrafo | `<p>Texto normal</p>` |
| `<a>` | Enlace | `<a href="pagina.html">Click aquí</a>` |
| `<img>` | Imagen | `<img src="foto.jpg" alt="Descripción">` |
| `<div>` | Contenedor genérico | `<div>Contenido agrupado</div>` |
| `<span>` | Contenedor en línea | `<span>Texto especial</span>` |
| `<ul>` y `<li>` | Lista no ordenada | `<ul><li>Item 1</li></ul>` |
| `<ol>` y `<li>` | Lista ordenada | `<ol><li>Primero</li></ol>` |

## 🎯 Atributos

Las etiquetas pueden tener **atributos** que dan información adicional:

```html
<a href="https://google.com" target="_blank">Ir a Google</a>
```

En este ejemplo:
- `href` es un atributo que indica la dirección del enlace
- `target="_blank"` indica que se abre en una nueva pestaña

### Atributos comunes:
- `id`: identificador único
- `class`: clase para aplicar estilos
- `src`: fuente de una imagen o archivo
- `href`: dirección de un enlace
- `alt`: texto alternativo para imágenes
- `title`: texto que aparece al pasar el mouse

## 📄 Estructura Básica de un Documento HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Título de la Página</title>
</head>
<body>
    <h1>Mi Primera Página</h1>
    <p>Este es el contenido visible de la página.</p>
</body>
</html>
```

### Explicación:
- `<!DOCTYPE html>`: Declara que este es un documento HTML5
- `<html>`: Etiqueta raíz que contiene todo
- `<head>`: Información sobre la página (no visible)
- `<meta charset="UTF-8">`: Codificación de caracteres (para acentos, ñ, etc.)
- `<title>`: Título que aparece en la pestaña del navegador
- `<body>`: Contenido visible de la página

## ✨ Importante Recordar

1. HTML **NO** es un lenguaje de programación, es de **marcado**
2. HTML define la **estructura**, no el diseño visual (eso es CSS)
3. Las etiquetas deben **cerrarse** (excepto algunas como `<img>`, `<br>`, `<input>`)
4. La **indentación** (espacios) ayuda a leer el código, pero no es obligatoria

## 🎯 Próximo Paso

Abre `ejercicio.html` en tu navegador y luego en un editor de texto para ver ejemplos prácticos.
