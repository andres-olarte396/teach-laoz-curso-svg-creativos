# EVALUACIÓN: INTERACTIVIDAD BÁSICA

## CUESTIONARIO

### Pregunta 1: El Fantasma Táctil
Quieres que un texto que está ENCIMA de un botón NO capture el clic, para que el clic pase directo al botón de abajo. ¿Qué propiedad CSS usas en el texto?

- [ ] a) `user-select: none`
- [ ] b) `pointer-events: none`
- [ ] c) `click-through: true`
- [ ] d) `z-index: -1`

### Pregunta 2: CSS vs JS
¿Cuál de estas interacciones se puede lograr SOLAMENTE con CSS (sin JavaScript)?

- [ ] a) Cambiar el color de un círculo al pasar el mouse por encima.
- [ ] b) Hacer que al hacer clic en un círculo, aparezca un texto nuevo en otra parte de la pantalla.
- [ ] c) Guardar el estado "seleccionado" de un botón permanentemente después de soltar el clic.

### Pregunta 3: UI Feedback
¿Cuál es la práctica estándar para indicar que un elemento SVG es clicable en escritorio?

- [ ] a) Ponerle un borde rojo.
- [ ] b) Usar `cursor: pointer`.
- [ ] c) Hacerlo parpadear.

---

## SOLUCIONARIO

### Pregunta 1: Solución
**Respuesta**: b) `pointer-events: none`.
**Explicación**: Esta propiedad hace que el elemento sea "transparente" a los eventos del mouse. Los clics atraviesan el elemento y actúan sobre lo que haya debajo.

### Pregunta 2: Solución
**Respuesta**: a) Cambiar el color al pasar el mouse.
**Explicación**: Esto se hace con la pseudo-clase `:hover`. Las opciones (b) y (c) implican lógica de estado persistente o manipulación del DOM externo al elemento disparador, lo cual requiere JS (o trucos muy avanzados de checkbox hack, pero no es estándar simple).

### Pregunta 3: Solución
**Respuesta**: b) Usar `cursor: pointer`.
**Explicación**: El cambio del cursor de flecha a mano es el indicador universal en la web de interactividad.
