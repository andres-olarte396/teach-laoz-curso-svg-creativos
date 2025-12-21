# BANCO DE EJERCICIOS: MÁSCARAS Y RECORTES

## METADATA
- **Módulo**: Estilizado Avanzado y Efectos
- **Tiempo total estimado**: 50 minutos
- **Nivel de ruta**: Avanzada

---

## EJERCICIO 1: El Catalejo (ClipPath)

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: `clipPath`, `circle`.

### ENUNCIADO
Dibuja un paisaje complejo (ej. un rectángulo verde para el suelo y uno azul para el cielo, con un sol amarillo).
Luego, aplica un `clipPath` circular en el centro para simular que estás viendo ese paisaje a través de un telescopio.
Todo lo que esté fuera del círculo debe desaparecer.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 200">
  <defs>
    <clipPath id="lente">
      <circle cx="100" cy="100" r="80" />
    </clipPath>
  </defs>
  
  <g clip-path="url(#lente)">
    <!-- Paisaje -->
    <rect width="200" height="200" fill="skyblue" />
    <rect y="150" width="200" height="50" fill="green" />
    <circle cx="150" cy="50" r="30" fill="yellow" />
  </g>
</svg>
```

---

## EJERCICIO 2: El Fantasma (Mask)

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `mask`, `linearGradient`, luminancia.

### ENUNCIADO
Dibuja un "fantasma" (un círculo o forma blanca sobre fondo negro).
Usa una máscara con un gradiente lineal (Blanco arriba -> Negro abajo) para que el fantasma se desvanezca suavemente hacia sus pies hasta desaparecer.
El fondo del SVG debe ser oscuro para apreciar el efecto.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 200" style="background: #222">
  <defs>
    <linearGradient id="g-alpha" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="white" /> <!-- Visible -->
      <stop offset="100%" stop-color="black" /> <!-- Invisible -->
    </linearGradient>
    
    <mask id="m-fantasma">
      <!-- El rect de la máscara debe cubrir al objeto -->
      <rect width="200" height="200" fill="url(#g-alpha)" />
    </mask>
  </defs>
  
  <circle cx="100" cy="80" r="50" fill="white" mask="url(#m-fantasma)" />
</svg>
```

---

## EJERCICIO 3: Texto de Recorte (Knockout Text)

### METADATA
- **Dificultad**: ⭐⭐⭐ Avanzado
- **Conceptos evaluados**: Texto en `mask` o `clipPath`.

### ENUNCIADO
Queremos ver una imagen (o un patrón de colores) SOLAMENTE a través de las letras de una palabra.
1. Escribe la palabra "SVG" gorda y centrada.
2. Usa esa palabra como `clipPath` para una serie de rayas de colores o una imagen de fondo.
El resultado debe ser que las letras tienen "relleno de rayas/imagen".

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 300 100">
  <defs>
    <clipPath id="texto-knockout">
      <text x="150" y="80" font-size="80" font-weight="bold" text-anchor="middle">
        SVG
      </text>
    </clipPath>
  </defs>
  
  <g clip-path="url(#texto-knockout)">
    <!-- Contenido de relleno -->
    <rect width="300" height="100" fill="red" />
    <rect width="300" height="50" fill="blue" />
    <circle cx="150" cy="50" r="40" fill="yellow" />
  </g>
</svg>
```
