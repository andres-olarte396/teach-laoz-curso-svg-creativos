# GUIÓN: PRIMITIVAS DE FORMA BÁSICA

## FICHA TÉCNICA
- **Duración**: 4-5 minutos
- **Tono**: Entusiasta, didáctico y directo.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**: (Amable y enérgico)
¡Hola! Bienvenido al módulo uno. Antes de empezar a correr, vamos a aprender a caminar geométricamente.
Hoy descubriremos las "Primitivas SVG". Piensa en ellas como plantillas o estarcidos que ya vienen listos en tu caja de herramientas.

¿Por qué complicarte calculando cuatro líneas perfectas para hacer un cuadrado, si puedes simplemente pedirle al navegador un "Rectángulo"?

---

### 00:45 - EL RECTÁNGULO Y EL CÍRCULO

**[LOCUTOR]**:
Empecemos por lo básico. El elemento `rect`.
Para dibujar uno, solo necesitas decirle dónde empieza, es decir, su `x` y su `y`, y por supuesto, su `width` y `height`.
¿Quieres esquinas redondeadas? Fácil, usa los atributos `rx` y `ry`. Es así de directo.

Ahora, mira el círculo. Aquí cambia un poco la lógica.
No definimos una esquina, sino el centro exacto: `cx` y `cy`. Y luego, el radio `r`.
(Pausa breve)
¡Ojo aquí! Un error clásico es intentar usar `x` e `y` en un círculo. El navegador te ignorará olímpicamente. Círculo usa centro, rectángulo usa esquina.

---

### 01:45 - ELIPSE Y LÍNEAS

**[LOCUTOR]**:
¿Y si quieres un círculo aplastado? Entonces usas `ellipse`.
Es igual que el círculo, pero en lugar de un solo radio, tienes dos: radio `x` y radio `y`.

Para dibujar líneas rectas, tenemos el elemento `line`. Punto A (`x1, y1`) a Punto B (`x2, y2`). Sencillo, ¿verdad?

---

### 02:30 - POLÍGONOS

**[LOCUTOR]**:
Ahora subamos el nivel. ¿Qué pasa si quieres un triángulo, una estrella o un hexágono?
Ahí entra el `polygon`.
Aquí simplemente le das una lista de coordenadas en el atributo `points`. El navegador conectará los puntos en orden y, esto es clave, cerrará la forma automáticamente, conectando el último punto con el primero.

---

### 03:15 - CONCLUSIÓN

**[LOCUTOR]**:
Estas son tus piezas de Lego fundamentales.
Rectángulos, círculos, elipses, líneas y polígonos.
Aunque más adelante veremos el todopoderoso `path`, que puede dibujarlo todo, usar estas primitivas hace que tu código sea legible y eficiente.

¡Ahora es tu turno de ponerlas en práctica en el editor! Nos vemos en la siguiente lección.
