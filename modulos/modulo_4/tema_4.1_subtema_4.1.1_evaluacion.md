# EVALUACIÓN: PLANIFICACIÓN Y DISEÑO

## CUESTIONARIO

### Pregunta 1: Orden de Capas
En un archivo SVG, si escribes primero el código del `Fondo` y después el código del `Botón`, ¿cuál aparece encima visualmente?

- [ ] a) El Fondo (quedan en orden inverso).
- [ ] b) El Botón (principio del pintor: lo último tapa a lo anterior).
- [ ] c) Depende de su `z-index`.

### Pregunta 2: Uso de Defs
¿Cuál es la razón principal para mover una forma compleja dentro de `<defs>`?

- [ ] a) Para que se dibuje automáticamente en el centro.
- [ ] b) Para ocultarla y poder reutilizarla/clonarla múltiples veces sin repetir código.
- [ ] c) Para mejorar el color.

### Pregunta 3: Estructura Mantenible
Si estás construyendo una interfaz compleja, ¿qué es mejor práctica?

- [ ] a) Poner todos los paths en la raíz para ahorrar caracteres.
- [ ] b) Agrupar elementos relacionados en `<g>` con IDs descriptivos (`id="menu"`, `id="logo"`).
- [ ] c) Usar múltiples archivos SVG y unirlos con iframes.

---

## SOLUCIONARIO

### Pregunta 1: Solución
**Respuesta**: b) El Botón.
**Explicación**: El "Painter's Algorithm" de SVG dicta que los elementos se dibujan en el orden en que aparecen en el DOM. Lo último pintado queda encima.

### Pregunta 2: Solución
**Respuesta**: b) Reutilización y optimización.
**Explicación**: `<defs>` permite definir objetos que no se renderizan hasta que son llamados con `<use>`. Esto es clave para patrones DRY.

### Pregunta 3: Solución
**Respuesta**: b) Agrupar con IDs descriptivos.
**Explicación**: La agrupación semántica facilita la lectura, el mantenimiento, y sobre todo, la manipulación posterior con CSS o JavaScript (puedes mover o ocultar todo el grupo "menú" de una sola vez).
