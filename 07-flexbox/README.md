# Flexbox - Layout Flexible

## 📐 ¿Qué es Flexbox?

**Flexbox** (Flexible Box Layout) es un sistema de diseño que facilita la alineación y distribución de elementos, incluso cuando sus tamaños son desconocidos o dinámicos.

Flexbox funciona en **una dimensión** a la vez: horizontal (fila) o vertical (columna).

## 🎯 Conceptos Básicos

### Contenedor Flex (Flex Container)
El elemento padre que tiene `display: flex`.

### Items Flex (Flex Items)
Los hijos directos del contenedor flex.

```html
<div class="contenedor">  <!-- Flex Container -->
    <div>Item 1</div>      <!-- Flex Item -->
    <div>Item 2</div>      <!-- Flex Item -->
    <div>Item 3</div>      <!-- Flex Item -->
</div>
```

```css
.contenedor {
    display: flex;
}
```

## 📦 Propiedades del Contenedor Flex

### 1. flex-direction (Dirección)
Define la dirección del eje principal.

```css
.contenedor {
    display: flex;
    flex-direction: row;          /* Por defecto: horizontal → */
    flex-direction: row-reverse;  /* Horizontal invertido ← */
    flex-direction: column;       /* Vertical ↓ */
    flex-direction: column-reverse; /* Vertical invertido ↑ */
}
```

### 2. justify-content (Alineación en eje principal)
Alinea items a lo largo del eje principal.

```css
.contenedor {
    display: flex;
    justify-content: flex-start;    /* Inicio (por defecto) */
    justify-content: flex-end;      /* Final */
    justify-content: center;        /* Centro */
    justify-content: space-between; /* Espacio entre items */
    justify-content: space-around;  /* Espacio alrededor */
    justify-content: space-evenly;  /* Espacio uniforme */
}
```

### 3. align-items (Alineación en eje transversal)
Alinea items en el eje perpendicular.

```css
.contenedor {
    display: flex;
    align-items: stretch;    /* Estirar (por defecto) */
    align-items: flex-start; /* Arriba */
    align-items: flex-end;   /* Abajo */
    align-items: center;     /* Centro */
    align-items: baseline;   /* Línea base del texto */
}
```

### 4. flex-wrap (Envolver)
Permite que los items pasen a la siguiente línea.

```css
.contenedor {
    display: flex;
    flex-wrap: nowrap;     /* No envolver (por defecto) */
    flex-wrap: wrap;       /* Envolver */
    flex-wrap: wrap-reverse; /* Envolver invertido */
}
```

### 5. gap (Espaciado)
Espacio entre items (moderna y muy útil).

```css
.contenedor {
    display: flex;
    gap: 20px;           /* 20px entre todos los items */
    gap: 10px 20px;      /* 10px vertical, 20px horizontal */
}
```

## 🎨 Propiedades de los Items Flex

### 1. flex-grow (Crecer)
Cuánto puede crecer un item respecto a otros.

```css
.item {
    flex-grow: 0;  /* No crece (por defecto) */
    flex-grow: 1;  /* Crece proporcionalmente */
    flex-grow: 2;  /* Crece el doble que flex-grow: 1 */
}
```

### 2. flex-shrink (Encoger)
Cuánto puede encogerse un item si falta espacio.

```css
.item {
    flex-shrink: 1;  /* Puede encogerse (por defecto) */
    flex-shrink: 0;  /* No se encoge */
}
```

### 3. flex-basis (Tamaño base)
Tamaño inicial del item antes de distribuir espacio.

```css
.item {
    flex-basis: auto;   /* Basado en contenido (por defecto) */
    flex-basis: 200px;  /* 200px de ancho/alto inicial */
    flex-basis: 50%;    /* 50% del contenedor */
}
```

### 4. flex (Atajo)
Combina grow, shrink y basis.

```css
.item {
    flex: 1;              /* flex-grow: 1, flex-shrink: 1, flex-basis: 0% */
    flex: 0 0 200px;      /* No crece, no encoge, 200px de base */
    flex: 2;              /* Crece el doble que flex: 1 */
}
```

### 5. align-self (Alineación individual)
Sobrescribe align-items para un item específico.

```css
.item {
    align-self: auto;       /* Hereda align-items */
    align-self: flex-start;
    align-self: center;
    align-self: flex-end;
}
```

## 🎯 Patrones Comunes

### Centrar completamente un elemento
```css
.contenedor {
    display: flex;
    justify-content: center;  /* Centro horizontal */
    align-items: center;      /* Centro vertical */
    height: 100vh;            /* Altura completa */
}
```

### Tres columnas iguales
```css
.contenedor {
    display: flex;
    gap: 20px;
}

.item {
    flex: 1;  /* Todos crecen igual */
}
```

### Navbar con logo a la izquierda y menú a la derecha
```css
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

### Cards responsivos
```css
.contenedor {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}

.card {
    flex: 1 1 300px;  /* Mínimo 300px, crece y envuelve */
}
```

## 💡 Consejos

1. **Empieza simple:** Usa `display: flex` y `gap` para la mayoría de casos
2. **Centrar es fácil:** `justify-content: center` + `align-items: center`
3. **Usa flex: 1 para columnas iguales**
4. **flex-wrap: wrap para layouts responsivos**
5. **gap es tu amigo:** Evita usar margin entre flex items

## ⚠️ Errores Comunes

1. **Olvidar display: flex en el contenedor**
   - Las propiedades flex solo funcionan si el padre tiene `display: flex`

2. **Confundir justify-content con align-items**
   - `justify-content` = eje principal (horizontal por defecto)
   - `align-items` = eje transversal (vertical por defecto)

3. **No usar flex-wrap cuando es necesario**
   - Los items se comprimirán en lugar de pasar a la siguiente línea

## 🎯 Próximo Paso

Abre `ejercicio-flexbox.html` para practicar con ejemplos interactivos.
