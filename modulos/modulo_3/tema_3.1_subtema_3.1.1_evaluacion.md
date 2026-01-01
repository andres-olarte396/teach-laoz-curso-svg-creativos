# EVALUACIÓN: ANIMACIÓN CON CSS

## CUESTIONARIO

### Pregunta 1: El Eje Loco

Estás animando una rotación `rotate(360deg)` en un SVG y el objeto, en lugar de girar sobre sí mismo, está dando vueltas enormes alrededor de la esquina de la pantalla. ¿Qué propiedad CSS te falta probablemente ajustar?

- [ ] a) `rotation-point: center`
- [ ] b) `transform-origin` y `transform-box`
- [ ] c) `top` y `left`

### Pregunta 2: El Truco del Trazo

¿Qué dos propiedades se combinan para crear el efecto de "autodibujado" de líneas?

- [ ] a) `stroke-width` y `stroke-color`
- [ ] b) `stroke-dasharray` y `stroke-dashoffset`
- [ ] c) `draw-path` y `draw-time`

### Pregunta 3: Límites de CSS

¿Puedes usar animaciones CSS (`@keyframes`) para transformar suavemente un Cuadrado en un Círculo modificando el atributo `d` del path?

- [ ] a) Sí, siempre funciona perfectamente en todos los navegadores.
- [ ] b) No, CSS no puede tocar el atributo `d`.
- [ ] c) Es posible en navegadores modernos (Chrome), pero compatible con riesgos y requiere mismo número de puntos.

---

## SOLUCIONARIO

### Pregunta 1: Solución

**Respuesta**: b) `transform-origin` y `transform-box`.
**Justificación**: Por defecto, SVG usa el `userSpaceOnUse` (el lienzo) para transformar. `transform-box: fill-box` le dice "usa la cajita del objeto" y `transform-origin: center` le dice "el centro de esa cajita".

### Pregunta 2: Solución

**Respuesta**: b) `stroke-dasharray` y `stroke-dashoffset`.
**Justificación**: `dasharray` crea el patrón de líneas y huecos. `dashoffset` mueve ese patrón.

### Pregunta 3: Solución

**Respuesta**: c) Es posible con riesgos.
**Justificación**: La interpolación de paths (`d: path(...)`) es una característica nueva en CSS. Funciona en Chromium pero falla o salta bruscamente en otros motores si la estructura de los paths no es idéntica (mismo número y tipo de comandos).
