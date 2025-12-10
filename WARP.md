# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Repository Overview

This is a **teaching repository** for an incremental HTML and CSS course designed for complete beginners. The course is in Spanish and follows a structured, step-by-step approach with heavy emphasis on visual learning.

**Target audience:** Students just starting in programming with no prior experience.
**Language:** Spanish (all documentation, comments, and content)
**Focus:** Foundational web development concepts, especially the Box Model

## Repository Structure

The repository contains 8 numbered modules that must be completed sequentially:

```
01-que-es-html/          - HTML fundamentals (tags, attributes, structure)
02-que-es-css/           - CSS basics (selectors, properties, linking)
03-que-es-javascript/    - Conceptual JavaScript intro (no programming)
04-estructura-proyecto/  - Project organization (separating HTML/CSS/JS files)
05-box-model/            - Box Model (margin, padding, width) ⭐ CRITICAL MODULE
06-positions/            - CSS positioning (static, relative, absolute, fixed, sticky)
07-flexbox/              - Flexbox layout system
08-calculadora/          - Final project: visual calculator (HTML + CSS only)
```

Each module contains:
- `README.md` - Theoretical explanations with visual diagrams
- `ejercicio.html` or similar - Practical exercises
- Additional example files as needed

## Key Teaching Concepts

### Critical Learning Point: Box Model (Module 05)
The Box Model is the most confusing concept for students. Use these teaching strategies:

**Analogy:** Each HTML element is a gift box
- **Content** = the gift inside
- **Padding** = protective paper around gift (INSIDE, has background color)
- **Border** = the box itself
- **Margin** = space between boxes (OUTSIDE, transparent)

**Key distinction:**
- PADDING = interior space, has element's background color, makes element larger
- MARGIN = exterior space, transparent, separates from other elements

**Golden rule question:** "Do you want the CONTENT to have more space (padding) or the BOX to be more SEPARATED (margin)?"

### Box Sizing
Always use `box-sizing: border-box` to make width calculations predictable:
```css
* {
    box-sizing: border-box;
}
```

### Common Patterns
**Centering horizontally:**
```css
.element {
    width: 500px;
    margin: 0 auto;
}
```

**Centering with Flexbox:**
```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
```

## Commands

### Viewing HTML Files
```bash
# Open any HTML file in default browser
open {{module}}/ejercicio.html
```

### Project Navigation
Files should be opened sequentially by module number. There is no build system, compilation, or test suite - this is pure HTML/CSS learning.

## Code Style

### HTML
- Always include proper document structure (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`)
- Use semantic tags where appropriate
- Include `<meta charset="UTF-8">` for Spanish characters (á, é, í, ó, ú, ñ)
- Use `lang="es"` attribute on `<html>` tag

### CSS
- Prefer external stylesheets or `<style>` tags in `<head>`
- Use meaningful class names in Spanish
- Always include `box-sizing: border-box` reset
- Comment complex CSS for student understanding
- Use visual examples with colored backgrounds to demonstrate concepts

### Comments
- All comments must be in Spanish
- Explain WHY, not just WHAT
- Include visual analogies when explaining Box Model or positioning

## Teaching Philosophy

1. **Incremental:** Never skip modules - learning builds on previous concepts
2. **Visual:** Always demonstrate in browser with DevTools (F12)
3. **Practical:** Theory followed by hands-on exercises
4. **Patient:** Box Model confusion is normal and expected
5. **No JavaScript functionality:** Projects are visual only until JS module

## Browser DevTools

The course heavily relies on browser DevTools for teaching:
- Press F12 to open DevTools
- Inspect Element shows the Box Model visualization
- Students should modify values live in DevTools to see effects
- Use computed styles to understand actual rendered values

## Common Student Mistakes

1. **Confusing padding with margin** (most common)
   - Solution: Use background colors to visualize the difference
   
2. **Forgetting `box-sizing: border-box`**
   - Without it, width doesn't include padding/border
   
3. **Using `width: 100%` with padding**
   - Causes overflow without `box-sizing: border-box`

4. **Forgetting to close tags**
   - HTML is forgiving but creates layout issues

5. **Not activating Flexbox with `display: flex`**
   - Flex properties only work on flex containers

## Final Project (Module 08)

The calculator project combines all concepts:
- **Structure:** HTML with proper semantic elements
- **Box Model:** Padding/margin for spacing, width/height for button sizing
- **Flexbox:** Layout for button grid and alignment
- **Styling:** Colors, borders, hover effects

The calculator is **visual only** - no JavaScript functionality. It's about applying CSS concepts, not programming logic.

## Files to Preserve

- `GUIA_PROFESOR.md` - Detailed instructor guide with session plans and teaching strategies
- `README.md` - Course overview and student instructions
- All module `README.md` files - Core teaching content
- All `ejercicio*.html` files - Practical exercises

## When Editing Files

- Maintain Spanish language throughout
- Keep visual analogies and diagrams
- Preserve incremental difficulty progression
- Use comments generously for student understanding
- Test all HTML files in browser before committing
- Ensure exercises are achievable for absolute beginners
