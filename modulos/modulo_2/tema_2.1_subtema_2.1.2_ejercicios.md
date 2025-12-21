# BANCO DE EJERCICIOS: GRADIENTES

## METADATA
- **Módulo**: Estilizado Avanzado y Efectos
- **Tiempo total estimado**: 50 minutos
- **Nivel de ruta**: Intermedia

---

## EJERCICIO 1: El Botón Metálico (Linear)

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: `linearGradient` vertical.

### ENUNCIADO
Crea un botón rectangular con efecto cilíndrico metálico.
Usa un gradiente lineal vertical (`x1=0, x2=0, y1=0, y2=1`) con 3 paradas:
1. Arriba: Gris claro (#ddd).
2. Medio: Blanco (#fff) (Brillo).
3. Abajo: Gris oscuro (#999).

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 60">
  <defs>
    <linearGradient id="metal" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#ddd" />
      <stop offset="50%" stop-color="#fff" />
      <stop offset="100%" stop-color="#999" />
    </linearGradient>
  </defs>
  <rect width="200" height="60" rx="10" fill="url(#metal)" stroke="#666" />
</svg>
```

---

## EJERCICIO 2: El Ojo de Sauron (Radial + Focal)

### METADATA
- **Dificultad**: ⭐⭐⭐ Avanzado
- **Conceptos evaluados**: `radialGradient`, `fx/fy`.

### ENUNCIADO
Dibuja un círculo rojo oscuro.
Aplica un gradiente radial que vaya de Amarillo (centro) a Rojo (borde).
**RETO**: Mueve el punto focal (`fx`, `fy`) para que el brillo amarillo no esté en el centro geométrico, sino desplazado hacia arriba, como si la pupila mirara hacia arriba.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 100 100">
  <defs>
    <!-- fx, fy desplazan el "origen" del color interno -->
    <radialGradient id="ojo" cx="50%" cy="50%" r="50%" fx="50%" fy="30%">
      <stop offset="0%" stop-color="yellow" />
      <stop offset="20%" stop-color="orange" />
      <stop offset="100%" stop-color="#330000" />
    </radialGradient>
  </defs>
  <circle cx="50" cy="50" r="45" fill="url(#ojo)" />
</svg>
```

---

## EJERCICIO 3: Bandera Arcoíris (Hard Stops)

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: Transiciones duras en gradientes.

### ENUNCIADO
Crea una bandera de 3 franjas verticales: Azul, Blanco, Rojo.
Debes usar **UN SOLO rectángulo** y **UN SOLO gradiente lineal** horizontal.
No vale usar 3 rectángulos separados.
Pista: Usa dos `stops` por cada punto de transición (ej. Azul hasta 33%, Blanco desde 33%).

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 300 200">
  <defs>
    <linearGradient id="francia" x1="0" y1="0" x2="1" y2="0">
      <stop offset="33%" stop-color="blue" />
      <stop offset="33%" stop-color="white" /> <!-- Cambio brusco -->
      <stop offset="66%" stop-color="white" />
      <stop offset="66%" stop-color="red" />   <!-- Cambio brusco -->
    </linearGradient>
  </defs>
  <rect width="300" height="200" fill="url(#francia)" />
</svg>
```
