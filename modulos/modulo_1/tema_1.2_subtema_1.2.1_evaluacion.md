# EVALUACIÓN: DOMINANDO EL ELEMENTO PATH (LINEALES)

## CUESTIONARIO

### Pregunta 1: El código secreto
¿Qué hace el comando `Z` al final de un path?

- [ ] a) Deshace la última línea.
- [ ] b) Dibuja una línea en forma de Z.
- [ ] c) Cierra el trazado conectando el punto actual con el punto de inicio.

### Pregunta 2: Relatividad
Si estoy en `(50, 50)` y ejecuto el comando `l 10 0` (ele minúscula), ¿dónde termina mi pluma?

- [ ] a) En `(10, 0)`
- [ ] b) En `(60, 50)`
- [ ] c) En `(10, 50)`

### Pregunta 3: Sintaxis
Señala el path VÁLIDO:

- [ ] a) `<path d="M 10 10 L 50 50" />`
- [ ] b) `<path points="10,10 50,50" />`
- [ ] c) `<path x="10" y="10" to="50,50" />`

---

## SOLUCIONARIO

### Pregunta 1: Solución
**Respuesta**: c) Cierra el trazado.
**Explicación**: `Z` (o `z`) traza una línea recta desde donde estés hasta el primer punto definido por el último comando `M`. Es esencial para colorear formas correctamente.

### Pregunta 2: Solución
**Respuesta**: b) En `(60, 50)`.
**Explicación**: `l` (minúscula) suma sus valores a la posición actual. `50 + 10 = 60` en X, `50 + 0 = 50` en Y.
Si fuera `L 10 0` (mayúscula), la respuesta sería a) `(10, 0)`.

### Pregunta 3: Solución
**Respuesta**: a) `<path d="M 10 10 L 50 50" />`
**Explicación**: El elemento path SOLO usa el atributo `d` para definir geometría. `points` es de `<polyline>`/`<polygon>`, y `x,y` no existen en path.
