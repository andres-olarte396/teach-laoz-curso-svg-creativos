# BANCO DE EJERCICIOS: GRUPOS Y TRANSFORMACIONES

## METADATA
- **Módulo**: Primitivas y Trazados
- **Tiempo total estimado**: 45 minutos
- **Nivel de ruta**: Intermedia

---

## EJERCICIO 1: El Sistema Solar

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `<g>`, `rotate`, `translate`.

### ENUNCIADO
Crea un modelo simplificado del sol y la tierra.
1. **Sol**: Círculo amarillo en el centro `(100, 100)`.
2. **Tierra**: Círculo azul pequeño orbitando.
3. **Reto**: Usa un grupo `<g>` para la Tierra. Dibuja la tierra en `(100, 50)` (arriba del sol). Luego, aplica una transformación `rotate(45, 100, 100)` al GRUPO para colocar la tierra en órbita de 45 grados sin calcular sus coordenadas x,y nuevas manualmente.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 200">
  <!-- Sol -->
  <circle cx="100" cy="100" r="20" fill="yellow" />
  
  <!-- Grupo Tierra rotado 45 grados sobre el centro del sol (100,100) -->
  <g transform="rotate(45, 100, 100)">
    <!-- Tierra en posición inicial (sin rotar) -->
    <circle cx="100" cy="50" r="10" fill="blue" />
  </g>
</svg>
```

---

## EJERCICIO 2: El Espejo (Scale negativo)

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `scale`, `transform-origin`.

### ENUNCIADO
Dibuja una flecha apuntando a la derecha (usando `polygon` o `line`).
Luego, usa `<use>` y `transform="scale(-1, 1)"` para crear una copia exacta que apunte a la izquierda (reflejo horizontal).
Nota: `scale(-1, 1)` voltea sobre el eje Y. Tendrás que trasladarlo de vuelta si se sale de la pantalla.

---

## EJERCICIO 3: ¿Qué pasa primero?

### ENUNCIADO
Dado el siguiente código:
`<rect x="0" y="0" width="10" height="10" transform="translate(50,0) rotate(45)" />`
Vs
`<rect x="0" y="0" width="10" height="10" transform="rotate(45) translate(50,0)" />`

Dibuja (en papel o mentalmente) dónde acaba cada cuadrado.
¿Son la misma posición? Justifica tu respuesta.
