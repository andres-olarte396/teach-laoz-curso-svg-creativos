# EVALUACIÓN: PRIMITIVAS DE FORMA BÁSICA

## CUESTIONARIO

### Instrucciones

Responde estas preguntas para comprobar que dominas los secretos de este nivel. ¡No mires las respuestas todavía!

### Pregunta 1: Cuestión de Centros

Estás dibujando un ojo robótico usando `<circle>`. Quieres que esté exactamente en la coordenada `(100, 100)`. ¿Qué atributos debes usar?

- a) `x="100" y="100"`
- b) `cx="100" cy="100"`
- c) `center-x="100" center-y="100"`

### Pregunta 2: El Rectángulo Desaparecido

Escribes `<rect x="10" y="10" width="0" height="50" />` pero no aparece nada en pantalla. ¿Por qué?

- a) El color de relleno por defecto es blanco.
- b) Falta el atributo de cierre `</rect>`.
- c) Una dimensión de 0 deshabilita el renderizado.

### Pregunta 3: Esquinas Suaves

Quieres que tu rectángulo tenga las esquinas redondeadas como un botón moderno. ¿Qué "herramienta" de tu estarcido usas?

- a) `border-radius`
- b) `round="true"`
- c) `rx` y `ry`

---

## SOLUCIONARIO

### Respuestas Explicadas

### Pregunta 1: Cuestión de Centros

**Respuesta Correcta**: b) `cx="100" cy="100"`

**¿Por qué?**:
Como vimos en la lección, los círculos se definen desde su centro (`cx`, `cy`). Los atributos `x` e `y` son para rectángulos (esquina superior izquierda).

### Pregunta 2: El Rectángulo Desaparecido

**Respuesta Correcta**: c) Una dimensión de 0 deshabilita el renderizado.

**¿Por qué?**:
La especificación SVG dicta que si el ancho o alto es 0, el elemento no se dibuja, incluso si tiene borde. Es como intentar cortar una tela con una regla de ancho cero.

### Pregunta 3: Esquinas Suaves

**Respuesta Correcta**: c) `rx` y `ry`

**¿Por qué?**:
Aunque `border-radius` es la forma de hacerlo en CSS, en la geometría del elemento SVG `<rect>`, usamos los radios `rx` (radio x) y `ry` (radio y) para definir la curvatura de las esquinas.
