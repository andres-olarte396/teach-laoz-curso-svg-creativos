# EVALUACIÓN: DOM

## CUESTIONARIO

### Pregunta 1: Naturaleza del DOM

¿Qué similitud tiene un `<rect>` SVG con un `<div>` HTML?

- a) Ninguna, son tecnologías opuestas.
- b) Ambos son nodos del DOM y pueden ser manipulados con JS/CSS. (Correcta)
- c) El `<rect>` solo puede ser manipulado por el servidor.

### Pregunta 2: Estilos

¿Cómo cambiarías el color de un SVG al pasar el mouse por encima?

- a) Es imposible, los SVG son estáticos.
- b) Usando la pseudo-clase `:hover` en CSS. (Correcta)
- c) Tienes que borrar el SVG y dibujar uno nuevo de otro color.

### Pregunta 3: Acceso

¿Puedo usar `document.getElementById('micirculo')` para seleccionar una parte de un dibujo SVG?

- a) Sí, siempre que tenga el atributo `id`. (Correcta)
- b) No, SVG usa una API separada.
- c) Solo si el SVG está incrustado como `<img src="...">`.

---

## SOLUCIONARIO

### Pregunta 1: Solución

**Respuesta**: b) Ambos son nodos del DOM.

### Pregunta 2: Solución

**Respuesta**: b) Usando `:hover`.
**Explicación**: Al ser elementos del DOM, aceptan estados CSS.

### Pregunta 3: Solución

**Respuesta**: a) Sí.
**Explicación**: El SVG (cuando es inline) comparte el mismo espacio de nombres DOM que el resto del documento HTML.
