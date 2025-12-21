# GUIÓN: DOMINANDO EL ELEMENTO PATH (LINEALES)

## FICHA TÉCNICA
- **Duración**: 4 minutos
- **Tono**: Técnico pero empoderador.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**:
Hasta ahora hemos jugado con sellos de goma: rectángulos, círculos. Muy bonitos, pero limitados.
Hoy soltamos los sellos y agarramos la pluma estilográfica.
Bienvenido al elemento `<path>`. El elemento más poderoso de SVG. Con él, puedes dibujar literalmente cualquier cosa.

---

### 00:45 - EL LENGUAJE DE LA PLUMA

**[LOCUTOR]**:
El path no usa atributos como x o width. Usa un solo atributo maestro: `d` (de "data").
Dentro de `d`, escribimos una serie de comandos de una letra. Imagina que diriges un robot:
- "M" (`Move to`): Levanta la pluma y ve a tal sitio.
- "L" (`Line to`): Baja la pluma y dibuja una línea hasta allá.
- "H" y "V": Atajos para líneas Horizontales y Verticales. Perfectos para dibujar cajas o escaleras.
- "Z": Cierra el camino, volviendo al punto de inicio.

---

### 02:00 - MAYÚSCULAS VS MINÚSCULAS

**[LOCUTOR]**:
Aquí está el secreto que confunde a muchos:
Las letras Mayúsculas (M, L) son coordenadas ABSOLUTAS. "Ve al pixel 100, 100".
Las minúsculas (m, l) son RELATIVAS. "Muévete 10 píxeles a la derecha desde donde estás".
Es la diferencia entre decir "Nos vemos en la Plaza Mayor" (Absoluto) y "Camina dos cuadras al norte" (Relativo).

---

### 03:00 - CONCLUSIÓN

**[LOCUTOR]**:
Al principio, el código del path parece una sopa de letras críptica.
`M10 10L50 50...`
Pero una vez que aprendes a leer "Move", "Line", "Close"... ves la forma en tu mente antes de que el navegador la renderice.
¡Vamos a trazar!
