# GUIÓN: GRADIENTES (LINEALES Y RADIALES)

## FICHA TÉCNICA
- **Duración**: 4-5 minutos
- **Tono**: Artístico y técnico.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**:
El mundo no es plano. Las cosas tienen volumen, luz, sombra.
Si usamos solo colores sólidos (`fill="red"`), nuestros diseños parecerán carteles de los años 50.
Para entrar en el siglo XXI, necesitamos profundidad. Necesitamos Gradientes.

---

### 00:30 - LA ANATOMÍA DEL GRADIENTE

**[LOCUTOR]**:
Un gradiente es simplemente una transición suave entre dos o más colores.
En SVG, al igual que los símbolos, los definimos en el "camerino" (`<defs>`).
Tenemos dos tipos:
1. **Lineal**: El color cambia a lo largo de una línea recta. Ideal para cielos, metales o sombras planas.
2. **Radial**: El color explota desde un punto central hacia afuera. Ideal para esferas, luces o brillos.

---

### 01:15 - LINEAR GRADIENT

**[LOCUTOR]**:
El `linearGradient` se controla con un vector `(x1, y1)` a `(x2, y2)`.
Si quieres un degradado horizontal, vas de izquierda a derecha. Si lo quieres vertical, de arriba a abajo.
Dentro del gradiente, colocamos "paradas" o `<stop>`.
"Al 0%, quiero azul. Al 100%, quiero rojo". Y el navegador se encarga de calcular los miles de tonos violetas intermedios.

---

### 02:00 - RADIAL GRADIENT

**[LOCUTOR]**:
El `radialGradient` es más divertido para efectos 3D.
Tienes un centro (`cx, cy`) y un radio (`r`).
Pero el truco de magia es el "Punto Focal" (`fx, fy`).
Si mueves el punto focal lejos del centro geométrico, creas la ilusión de que la luz viene de un lado, convirtiendo un círculo plano en una esfera tridimensional instantáneamente.

---

### 02:45 - UNIDADES

**[LOCUTOR]**:
¡Cuidado con las coordenadas! Por defecto, los gradientes hablan en porcentajes del objeto.
`x1="0"` es el borde izquierdo, `x1="1"` es el derecho.
No uses píxeles aquí a menos que sepas muy bien lo que haces.

---

### 03:15 - CIERRE

**[LOCUTOR]**:
Dominar los gradientes es dominar la iluminación.
Juega con las transparencias, superpón gradientes... convierte tu código en arte.
¡A pintar!
