# EVALUACIÓN: IMPLEMENTACIÓN Y REFINAMIENTO

## CUESTIONARIO

### Pregunta 1: El ViewBox
Si tu SVG tiene `width="100"` y `height="100"`.
Pero su `viewBox="0 0 50 50"`.
¿Cómo se verán los elementos dentro?

- [ ] a) Se verán a mitad de tamaño (pequeños).
- [ ] b) Se verán al doble de tamaño (Zoom in 2x).
- [ ] c) Se deformarán.

### Pregunta 2: Accesibilidad
¿Qué etiqueta es fundamental para que Google indexe tu SVG y los ciegos sepan qué es?

- [ ] a) `<meta name="description">`
- [ ] b) `<alt>`
- [ ] c) `<title>` y `<desc>` dentro del SVG.

### Pregunta 3: Performance
Si tienes 50 estrellas idénticas en tu cielo nocturno. ¿Qué es mejor para el rendimiento?

- [ ] a) Copiar y pegar el código del círculo 50 veces (`<circle>...`).
- [ ] b) Definir el círculo en `<defs>` y usar `<use>` 50 veces.
- [ ] c) Usar 50 imágenes `.png` incrustadas.

---

## SOLUCIONARIO

### Pregunta 1: Solución
**Respuesta**: b) Se verán al doble de tamaño (Zoom in 2x).
**Explicación**: El `viewBox` define "qué ventana del mundo estamos mirando". Si la ventana (0-50) es más pequeña que el marco donde se muestra (0-100), la imagen se estira para llenar el marco. Es como hacer zoom.

### Pregunta 2: Solución
**Respuesta**: c) `<title>` y `<desc>`.
**Explicación**: Son los estándares W3C para accesibilidad en SVG. Funcionan como el atributo `alt` de las imágenes.

### Pregunta 3: Solución
**Respuesta**: b) Usar `<use>`.
**Explicación**: Reduce el tamaño del DOM y permite al navegador optimizar el renderizado, ya que sabe que es la misma geometría repetida.
