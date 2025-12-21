# GUIÓN: ANIMACIÓN CON CSS

## FICHA TÉCNICA
- **Duración**: 5-6 minutos
- **Tono**: Dinámico y moderno.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**:
Un gráfico vectorial estático es hermoso. Pero un gráfico vectorial que se mueve, respira y cuenta una historia... eso es magia.
Y no necesitas aprender software complejo como After Effects.
Si sabes CSS, ya tienes la varita mágica.

---

### 00:45 - EL MOTOR @KEYFRAMES

**[LOCUTOR]**:
Todo empieza con la regla estándar de CSS: `@keyframes`.
Defines momentos en el tiempo: Inicio (0%) y Fin (100%).
¿Qué podemos animar? Casi todo lo que tenga que ver con "apariencia":
- Colores (`fill`, `stroke`) para hacer luces parpadeantes.
- Opacidad (`opacity`) para apariciones fantasmales.
- Y transformaciones (`scale`, `rotate`, `translate`) para mover cosas.

---

### 01:30 - EL TRUCO DEL TRAZO

**[LOCUTOR]**:
Pero hay un truco exclusivo de SVG que tienes que conocer. El "Efecto de Dibujado".
Funciona manipulando el borde de la línea (`stroke`).
1. Conviertes la línea continua en una línea punteada (`dasharray`).
2. Haces que el "punto" y el "espacio" sean tan largos como la línea entera.
3. Mueves el trazo (`dashoffset`) hasta que solo se vea el espacio vacío.
4. Animas ese desplazamiento a 0.
¡Voilá! La línea parece dibujarse sola.

---

### 02:15 - CUIDADO CON EL EJE

**[LOCUTOR]**:
Una advertencia crucial. Cuando rotas un DIV en HTML, rota sobre su centro. Fácil.
Cuando rotas un path en SVG, a veces rota sobre la esquina superior izquierda del lienzo y sale volando.
Para arreglarlo, recuerda este hechizo CSS:
`transform-box: fill-box;`
`transform-origin: center;`
Esto obliga al SVG a comportarse como un elemento HTML normal y rotar sobre su propio eje.

---

### 03:00 - CONCLUSIÓN

**[LOCUTOR]**:
La animación CSS es performante, ligera y funciona en todos lados.
Da vida a tus iconos. Haz que tus logos latan.
Pero recuerda: Un gran poder conlleva una gran responsabilidad. No marees al usuario con mil cosas moviéndose a la vez. Úsalo con sutileza.
