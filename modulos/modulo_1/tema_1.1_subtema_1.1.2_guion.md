# GUIÓN: GRUPOS Y TRANSFORMACIONES

## FICHA TÉCNICA
- **Duración**: 3-4 minutos
- **Tono**: Analítico pero accesible.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**:
Imagina que tienes que mover una casa entera. ¿Mueves los ladrillos uno por uno, o levantas la casa completa y la llevas a otro lado?
En SVG, el elemento `group` o `<g>` es esa capacidad de tratar múltiples objetos como uno solo.

---

### 00:45 - EL GRUPO <G>

**[LOCUTOR]**:
`<g>` no dibuja nada por sí mismo. Es un contenedor invisible.
Pero tiene dos superpoderes:
1. **Herencia**: Si le pones `fill="red"` al grupo, todos sus hijos serán rojos (a menos que digan lo contrario).
2. **Transformación conjunta**: Puedes rotar, escalar o mover todo el grupo a la vez.

---

### 01:30 - TRANSFORMACIONES

**[LOCUTOR]**:
Hablemos del atributo `transform`.
La función más común es `translate(x, y)`. Simplemente mueve el origen de coordenadas.
Luego está `rotate(grados)`.
Aquí hay una trampa: Por defecto, SVG rota sobre la esquina `(0,0)` del lienzo, ¡no sobre el centro del objeto!
Si quieres rotar un planeta sobre su eje, necesitas decirle dónde está ese eje: `rotate(45, cx, cy)`.

---

### 02:30 - EL ORDEN IMPORTA

**[LOCUTOR]**:
Finalmente, ten cuidado con el orden.
`translate` y luego `rotate` NO es lo mismo que `rotate` y luego `translate`.
Piensa en ello como caminar y luego girar, versus girar y luego caminar. Terminas en lugares muy distintos.
¡A experimentar con la caja mágica del grupo!
