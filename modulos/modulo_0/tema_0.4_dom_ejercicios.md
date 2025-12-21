# BANCO DE EJERCICIOS: EL DOM

## METADATA
- **Módulo**: 0 (Nivelación)
- **Tema**: DOM e Interactividad

---

## EJERCICIO 1: Selectores
### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: IDs y Clases.

### ENUNCIADO
Tienes el siguiente código:
```xml
<circle id="sol" fill="yellow" />
<rect class="edificio" fill="gray" />
<rect class="edificio" fill="gray" />
```

Escribe el selector CSS necesario para pintar los edificios de azul.

### SOLUCIÓN MODELO
```css
.edificio {
  fill: blue;
}
```
*Nota: En SVG usamos `fill`, no `background-color`.*

---

## EJERCICIO 2: La Jerarquía
### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: Árbol DOM.

### ENUNCIADO
Si aplicas `opacity: 0.5` a un grupo `<g>`, ¿qué le pasa a los rectángulos que están dentro de ese grupo?

1. Nada, solo el grupo se vuelve transparente.
2. Heredan la transparencia y se vuelven semitransparentes.
3. Se vuelven invisibles.

### SOLUCIÓN MODELO
**2. Heredan la transparencia.**
El estilo fluye en cascada por el DOM. Si el padre es semitransparente, los hijos también.
