# BANCO DE EJERCICIOS: SINTAXIS XML

## METADATA
- **Módulo**: 0 (Nivelación)
- **Tema**: XML y Sintaxis Estricta

---

## EJERCICIO 1: El Inspector de Errores

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: Well-formedness.

### ENUNCIADO
El siguiente código SVG está roto y no se renderiza. Encuentra los 3 errores de sintaxis XML.

```xml
<svg width=100 height="100">
  <Circle cx="50" cy="50" r="20" fill="red">
</svg>
```

### SOLUCIÓN MODELO
1. `width=100`: Falta comillas -> `width="100"`.
2. `<Circle>`: SVG es case-sensitive. Debe ser `<circle>`.
3. Etiqueta no cerrada: `<circle ... >` debe cerrarse con `/>` o `</circle>`.

Correcto:
```xml
<svg width="100" height="100">
  <circle cx="50" cy="50" r="20" fill="red" />
</svg>
```

---

## EJERCICIO 2: Anidamiento Lógico

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: Jerarquía de árbol.

### ENUNCIADO
Escribe la estructura XML para:
"Un grupo (`g`) que contiene un cuadrado (`rect`) y dentro del cuadrado (conceptualmente encima) un texto (`text`)".
Nota: En SVG, `rect` no puede tener hijos, así que deben ser hermanos dentro del grupo.

### SOLUCIÓN MODELO
```xml
<g>
  <rect width="100" height="100" />
  <text x="10" y="50">Hola</text>
</g>
```
*Si el alumno intenta poner `<rect><text>...</text></rect>`, está mal porque `rect` es un elemento vacío/primitivo.*
