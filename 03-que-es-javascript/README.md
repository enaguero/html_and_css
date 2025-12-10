# ¿Qué es JavaScript?

## 📖 Definición

**JavaScript** es un lenguaje de **programación** que permite hacer las páginas web **interactivas**.

Si HTML es el esqueleto y CSS es la apariencia, JavaScript es el **cerebro y los músculos** que hacen que la página responda a nuestras acciones.

## 🎯 ¿Para qué sirve?

JavaScript sirve para:
- **Responder a eventos** (clics, teclas presionadas, movimiento del mouse)
- **Modificar** el contenido de la página sin recargarla
- **Validar** formularios
- **Crear animaciones** complejas
- **Comunicarse** con servidores (cargar datos)
- **Crear aplicaciones web** completas

## 🧱 Diferencias con HTML y CSS

| Aspecto | HTML | CSS | JavaScript |
|---------|------|-----|------------|
| **Tipo** | Lenguaje de marcado | Lenguaje de estilos | Lenguaje de programación |
| **Función** | Estructura | Diseño visual | Interactividad y lógica |
| **Ejemplo** | `<button>Haz clic</button>` | `button { color: red; }` | `button.onclick = ...` |

## 💡 Ejemplos de Uso

### Ejemplo 1: Cambiar texto al hacer clic
```html
<button onclick="alert('¡Hola!')">Presióname</button>
```

### Ejemplo 2: Cambiar el contenido
```javascript
document.getElementById('titulo').textContent = 'Nuevo texto';
```

### Ejemplo 3: Validar un formulario
```javascript
if (email.includes('@')) {
    // El email es válido
}
```

## 🌐 ¿Dónde se ejecuta?

JavaScript se ejecuta en el **navegador web** del usuario (Chrome, Firefox, Safari, etc.). Esto se llama "JavaScript del lado del cliente".

También existe JavaScript del lado del servidor (Node.js), pero eso es más avanzado.

## 📌 ¿Cómo se conecta con HTML?

Hay 3 formas de agregar JavaScript:

### 1. Archivo externo (Recomendado)
```html
<script src="script.js"></script>
```

### 2. JavaScript interno
```html
<script>
    console.log('Hola desde JavaScript');
</script>
```

### 3. JavaScript en línea
```html
<button onclick="alert('Click!')">Botón</button>
```

## ⚠️ Para este Curso

**Importante:** En este curso nos enfocamos en **HTML y CSS**. JavaScript lo veremos solo de forma introductoria.

Los proyectos que haremos serán principalmente con HTML y CSS. La calculadora final será visual (sin funcionalidad de cálculo real).

## ✨ Conceptos Básicos de JavaScript

Aunque no programaremos en este curso, es útil conocer estos conceptos:

### Variables
```javascript
let nombre = "María";
let edad = 25;
```

### Funciones
```javascript
function saludar() {
    console.log("Hola");
}
```

### Condicionales
```javascript
if (edad > 18) {
    console.log("Es mayor de edad");
}
```

### Eventos
```javascript
button.addEventListener('click', function() {
    console.log('Botón presionado');
});
```

## 🎯 Lo Importante Ahora

Por ahora, lo más importante es que entiendas:

1. JavaScript es para **interactividad**
2. Es un **lenguaje de programación real** (a diferencia de HTML/CSS)
3. Trabaja **junto con** HTML y CSS
4. No necesitas dominarlo para crear páginas web bonitas

## 🎯 Próximo Paso

Abre `ejemplo.html` para ver algunos ejemplos simples de JavaScript en acción.
