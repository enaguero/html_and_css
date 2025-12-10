# Posiciones en CSS

## 📍 ¿Qué es Position?

La propiedad `position` controla **cómo** y **dónde** se posiciona un elemento en la página.

Por defecto, los elementos se posicionan en el **flujo normal** del documento (uno después del otro). Con `position` podemos cambiar esto.

## 🎯 Los 5 Valores de Position

### 1. **static** (Por Defecto)
Posición normal, en el flujo del documento.

```css
.elemento {
    position: static; /* Valor por defecto */
}
```

**Características:**
- Es el valor por defecto
- No se ve afectado por `top`, `right`, `bottom`, `left`
- Sigue el flujo normal del documento

---

### 2. **relative** (Relativo)
El elemento se posiciona **relativo a su posición original**.

```css
.elemento {
    position: relative;
    top: 20px;      /* Se mueve 20px hacia abajo desde su posición original */
    left: 30px;     /* Se mueve 30px hacia la derecha */
}
```

**Características:**
- Se mueve desde donde estaría normalmente
- **Mantiene su espacio** en el flujo del documento
- Puede salirse de su contenedor
- Sirve como referencia para elementos `absolute` dentro de él

**Uso común:** Ajustar ligeramente la posición de un elemento.

---

### 3. **absolute** (Absoluto)
El elemento se posiciona **relativo al ancestro más cercano con position distinto de static**.

```css
.contenedor {
    position: relative; /* Referencia */
}

.elemento {
    position: absolute;
    top: 10px;
    right: 10px;
}
```

**Características:**
- Se **saca del flujo** del documento (no ocupa espacio)
- Se posiciona respecto al primer padre con `position: relative` (o `absolute`, `fixed`)
- Si no hay padre posicionado, se posiciona respecto al `<body>`
- Otros elementos actúan como si no existiera

**Uso común:** Posicionar elementos precisamente (badges, tooltips, overlays).

---

### 4. **fixed** (Fijo)
El elemento se posiciona **relativo a la ventana del navegador**.

```css
.elemento {
    position: fixed;
    top: 0;
    right: 0;
}
```

**Características:**
- Se **saca del flujo** del documento
- Se posiciona respecto a la **ventana del navegador**
- Permanece en la misma posición aunque hagas scroll
- No se mueve con el resto del contenido

**Uso común:** Menús de navegación fijos, botones flotantes, avisos.

---

### 5. **sticky** (Pegajoso)
Mezcla entre `relative` y `fixed`. Cambia según el scroll.

```css
.elemento {
    position: sticky;
    top: 0;
}
```

**Características:**
- Actúa como `relative` hasta que llegas a un umbral de scroll
- Luego actúa como `fixed`
- Requiere especificar al menos `top`, `bottom`, `left` o `right`

**Uso común:** Encabezados de tabla que se quedan fijos al hacer scroll.

## 📐 Propiedades de Posicionamiento

Estas propiedades solo funcionan cuando `position` NO es `static`:

```css
.elemento {
    position: absolute; /* o relative, fixed, sticky */
    
    top: 10px;          /* Distancia desde arriba */
    right: 20px;        /* Distancia desde la derecha */
    bottom: 30px;       /* Distancia desde abajo */
    left: 40px;         /* Distancia desde la izquierda */
}
```

## 🎨 Z-Index (Profundidad)

Controla qué elemento aparece **encima** de otro cuando se superponen.

```css
.elemento-1 {
    position: absolute;
    z-index: 1;
}

.elemento-2 {
    position: absolute;
    z-index: 10; /* Este aparece ENCIMA del elemento-1 */
}
```

**Características:**
- Valores más altos = más arriba (encima)
- Solo funciona con elementos posicionados (no `static`)
- Por defecto es `auto` (orden del HTML)

## 🔍 Comparación Visual

```
STATIC (por defecto)
┌─────────┐
│ Elem 1  │
└─────────┘
┌─────────┐
│ Elem 2  │  ← Uno después del otro
└─────────┘

RELATIVE
┌─────────┐
│ Elem 1  │
└─────────┘
  ┌─────────┐
  │ Elem 2  │  ← Movido, pero deja espacio
  └─────────┘

ABSOLUTE
┌─────────┐
│ Elem 1  │
│  ┌───┐  │
│  │ 2 │  │  ← Dentro, sin afectar el flujo
│  └───┘  │
└─────────┘

FIXED
    ┌─────┐
    │  2  │   ← Siempre visible al hacer scroll
    └─────┘
┌─────────┐
│ Elem 1  │
└─────────┘
```

## 💡 Casos de Uso Comunes

### Centrar un elemento con absolute
```css
.centrado {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

### Navbar fijo en la parte superior
```css
nav {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: white;
    z-index: 100;
}
```

### Badge en esquina de un contenedor
```css
.contenedor {
    position: relative;
}

.badge {
    position: absolute;
    top: -10px;
    right: -10px;
}
```

## ⚠️ Errores Comunes

1. **Usar absolute sin contenedor relative**
   - El elemento se posicionará respecto al body
   - Solución: Dar `position: relative` al padre

2. **Olvidar especificar top/left/etc**
   - El elemento puede aparecer en lugares inesperados

3. **Problemas con z-index**
   - Solo funciona en elementos posicionados
   - Contextos de apilamiento pueden complicar esto

## 🎯 Próximo Paso

Abre `ejercicio-positions.html` para ver ejemplos interactivos de cada tipo de posición.
