# EVALUACIÓN: GRADIENTES

## CUESTIONARIO

### Pregunta 1: Dirección del Flujo

Si configuro un `<linearGradient>` con `x1="0" y1="0"` y `x2="0" y2="1"`, ¿en qué dirección fluye el cambio de color?

- a) Horizontal (Izquierda a Derecha)
- b) Vertical (Arriba a Abajo)
- c) Diagonal (Esquina a Esquina)

### Pregunta 2: El elemento Stop

¿Qué atributos son **obligatorios** dentro de un elemento `<stop>`?

- a) `color` y `position`
- b) `stop-code` y `stop-opacity`
- c) `offset` y `stop-color`

### Pregunta 3: Coordenadas Relativas

Si muevo y redimensiono un rectángulo que tiene aplicado un gradiente, ¿qué pasa con el gradiente (por defecto)?

- a) Se queda fijo en la pantalla (como un fondo de escritorio).
- b) Se mueve y estira junto con el rectángulo.
- c) Desaparece hasta que recalcules el gradiente.

---

## SOLUCIONARIO

### Pregunta 1: Solución

**Respuesta**: b) Vertical (Arriba a Abajo).
**Justificación**: `x` no cambia (0 a 0), solo cambia `y` (0 a 1). Por tanto, el vector apunta hacia abajo.

### Pregunta 2: Solución

**Respuesta**: c) `offset` y `stop-color`.
**Justificación**: `offset` dice "dónde" (ej 50%) y `stop-color` dice "qué color".

### Pregunta 3: Solución

**Respuesta**: b) Se mueve y estira junto con el rectángulo.
**Justificación**: Por defecto, `gradientUnits="objectBoundingBox"`. Esto significa que el sistema de coordenadas del gradiente es relativo a la caja del objeto (0 a 1). Si el objeto crece, el gradiente crece.
