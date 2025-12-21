# GUIÓN: CURVAS DE BÉZIER (C y Q)

## FICHA TÉCNICA
- **Duración**: 5-6 minutos
- **Tono**: Inspirador y detallado.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**:
Mira a tu alrededor. ¿Ves muchas líneas rectas perfectas en la naturaleza? Probablemente no. La vida es curva.
Y para dibujar la vida en SVG, necesitamos algo más sofisticado que una regla. Necesitamos las curvas de Bézier.

---

### 00:30 - EL CONCEPTO DE IMANES

**[LOCUTOR]**:
Imagina una cuerda elástica tensada entre dos puntos.
Si pongo un imán potente cerca de la cuerda, esta se curvará hacia él, ¿cierto? Pero nunca tocará el imán.
Ese es el principio de Bézier. Los "puntos de control" son esos imanes.

---

### 01:15 - Q vs C

**[LOCUTOR]**:
Tenemos dos sabores principales:
La Curva Cuadrática, o comando `Q`. Usa UN solo imán. Es perfecta para curvas simples, arcos suaves.
La Curva Cúbica, o comando `C`. Usa DOS imanes. Uno tira del principio y el otro tira del final. Esto te permite hacer curvas en forma de S o bucles complejos que una `Q` simplemente no puede lograr.

---

### 02:30 - CONTINUIDAD

**[LOCUTOR]**:
El mayor reto es cuando unes dos curvas. Si no tienes cuidado, crearás un pico, una esquina fea.
Para evitarlo, SVG nos da los comandos `S` y `T`. Estos calculan automáticamente dónde poner el primer imán de la siguiente curva para que la transición sea mantequilla pura.

---

### 03:00 - CONCLUSIÓN DEL MÓDULO 1

**[LOCUTOR]**:
¡Felicidades! Con esto cerramos el Módulo 1.
Ya tienes el poder de dibujar cualquier forma imaginable en el universo 2D.
Rectángulos, círculos, grupos y ahora, curvas libres.
En el próximo módulo, dejaremos de dibujar líneas y empezaremos a pintar. Entraremos en el mundo del color, los gradientes y las máscaras.
¡Descansa esos dedos y nos vemos pronto!
