# BANCO DE EJERCICIOS: ANIMACIÓN CON CSS

## METADATA
- **Módulo**: SVG Vivo - Animación e Interactividad
- **Tiempo total estimado**: 60 minutos
- **Nivel de ruta**: Intermedia

---

## EJERCICIO 1: El Semáforo (Cambio de color)

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: `@keyframes`, `fill`.

### ENUNCIADO
Dibuja un semáforo (3 círculos grises verticales).
Crea una animación CSS llamada `luz` que cambie el `fill` de un color apagado (#555) a un color encendido (Red/Yellow/Green).
Aplica la animación a cada círculo con retardos (`animation-delay`) para simular la secuencia:
1. Rojo se enciende (0s).
2. Rojo se apaga, Amarillo se enciende (2s).
3. Amarillo se apaga, Verde se enciende (3s).

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 100 300">
  <style>
    @keyframes parpadeo {
      0%, 100% { fill: #555; }
      50% { fill: currentColor; } /* Usa el color definido en el elemento */
    }
    
    .luz { animation: parpadeo 3s infinite; fill: #555; }
    
    #rojo { color: red; animation-delay: 0s; }
    #amarillo { color: yellow; animation-delay: 1s; }
    #verde { color: lime; animation-delay: 2s; }
  </style>
  
  <rect width="100" height="300" fill="#222" />
  <circle id="rojo" class="luz" cx="50" cy="50" r="40" />
  <circle id="amarillo" class="luz" cx="50" cy="150" r="40" />
  <circle id="verde" class="luz" cx="50" cy="250" r="40" />
</svg>
```

---

## EJERCICIO 2: El Planeta (Rotación)

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `transform`, `transform-origin`, `transform-box`.

### ENUNCIADO
Dibuja un planeta (círculo grande) y una luna (círculo pequeño) orbitando a su alrededor.
**RETO**: Usa CSS `transform: rotate()` para mover la luna.
**Truco**: Para que orbite alrededor del planeta (y no sobre sí misma), ajusta el `transform-origin` al centro del planeta.
O agrupa la luna en un `<g>`, centra el grupo en el planeta, y rota el grupo.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 200">
  <style>
    @keyframes orbita {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    .luna-grupo {
      animation: orbita 4s linear infinite;
      transform-origin: 100px 100px; /* Centro del sol */
    }
  </style>

  <!-- Sol -->
  <circle cx="100" cy="100" r="30" fill="gold" />

  <!-- Luna en un grupo para facilitar rotación -->
  <g class="luna-grupo">
    <circle cx="100" cy="40" r="10" fill="silver" />
  </g>
</svg>
```

---

## EJERCICIO 3: La Firma (Stroke Dasharray)

### METADATA
- **Dificultad**: ⭐⭐⭐ Avanzado
- **Conceptos evaluados**: `stroke-dasharray`, `stroke-dashoffset`.

### ENUNCIADO
"Firma" tu nombre usando una `<polyline>` o `<path>` (una línea garabateada simple sirve).
Usa el Inspector del navegador para medir la longitud aproximada del path (`path.getTotalLength()` en consola o a ojo).
Configura `stroke-dasharray` con esa longitud y anima `stroke-dashoffset` desde esa longitud hasta 0 para ver cómo se escribe sola.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 300 100">
  <style>
    @keyframes firmar {
      to { stroke-dashoffset: 0; }
    }
    .trazo {
      fill: none;
      stroke: black;
      stroke-width: 3;
      stroke-dasharray: 400; /* Asumiendo longitud 400 */
      stroke-dashoffset: 400; /* Escondido */
      animation: firmar 3s ease-out forwards;
    }
  </style>
  
  <!-- Una firma falsa -->
  <path class="trazo" d="M10 50 Q 50 10 90 50 T 170 50 T 250 50" />
</svg>
```
