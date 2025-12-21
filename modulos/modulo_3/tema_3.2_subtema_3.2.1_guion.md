# GUIÓN: INTERACTIVIDAD BÁSICA

## FICHA TÉCNICA
- **Duración**: 4-5 minutos
- **Tono**: Práctico y orientado a UX.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**:
Una web que no reacciona se siente rota.
Estamos acostumbrados a tocar, deslizar y hacer clic.
SVG no es un JPG estático. Es código vivo en el navegador. Y eso significa que puede sentir tus clics y responder.

---

### 00:30 - NIVEL 1: CSS (REFLEJOS)

**[LOCUTOR]**:
El primer nivel de interacción no requiere JavaScript. Son los "reflejos" del SVG.
Usamos pseudo-clases de CSS, igual que en cualquier botón HTML.
`:hover`: Para cuando pasas el mouse por encima. Cambia el color, aumenta la escala. Dile al usuario "¡Soy clicable!".
`:active`: Para el momento del clic. Haz que el botón se hunda un poco. Da feedback táctil.
Y no olvides `cursor: pointer`. Sin esa manita, nadie sabrá que es un botón.

---

### 01:15 - NIVEL 2: HITBOXES

**[LOCUTOR]**:
Un secreto de profesional: La Ley de Fitts.
Hacer clic en una línea de 1 pixel es una pesadilla de usabilidad.
¿La solución? Dibuja una forma transparente gruesa encima de tu línea fina.
El usuario verá la línea elegante, pero hará clic en la forma gorda invisible. Eso es una buena experiencia de usuario (UX).

---

### 02:00 - NIVEL 3: JAVASCRIPT (CEREBRO)

**[LOCUTOR]**:
Para cosas más complejas, como un mapa donde al hacer clic en un país sale su información, usamos JavaScript.
No necesitas librerías raras. Un simple `addEventListener('click')` funciona perfecto en cualquier elemento SVG.
Puedes cambiar atributos, lanzar animaciones, o cargar datos. El límite es tu imaginación.

---

### 03:00 - CONCLUSIÓN DEL CURSO (TEÓRICA)

**[LOCUTOR]**:
Con esto cerramos el ciclo técnico.
Has aprendido a trazar (Módulo 1), a pintar (Módulo 2) y a dar vida (Módulo 3).
Ahora tienes todas las piezas. Es hora de ensamblarlas.
En el próximo paso, tú serás el arquitecto. Vas a construir el Proyecto Final.
¡El editor te espera!
