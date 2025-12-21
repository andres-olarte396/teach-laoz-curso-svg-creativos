# BANCO DE EJERCICIOS: PRIMITIVAS DE FORMA BÁSICA

## METADATA
- **Módulo**: Primitivas y Trazados
- **Objetivos evaluados**: Dominio de sintaxis de rect, circle, ellipse, line, polygon.
- **Tiempo total estimado**: 45 minutos
- **Tipo**: Formativa
- **Nivel de ruta**: Básica/Intermedia

---

## EJERCICIO 1: La Bandera Geométrica

### METADATA
- **ID**: EJ-MOD1-001
- **Dificultad**: ⭐ Básico
- **Tiempo estimado**: 10 minutos
- **Nivel Bloom**: Aplicar
- **Conceptos evaluados**: `<rect>`, sistemas de coordenadas.

### ENUNCIADO
Dibuja la bandera de un país ficticio compuesta por:
1. Un fondo rectangular de 300x200 píxeles (color gris claro).
2. Una franja vertical roja a la izquierda (ancho 100px).
3. Una franja horizontal azul en la parte superior (alto 50px).
4. Un cuadrado verde en la intersección de las dos franjas anteriores.

**Restricciones**:
- Usar un `viewBox` de "0 0 300 200".
- Usar solo elementos `<rect>`.

**Output esperado**:
Un código SVG válido que visualice lo descrito.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 300 200" xmlns="http://www.w3.org/2000/svg">
  <!-- Fondo -->
  <rect x="0" y="0" width="300" height="200" fill="#ddd" />
  
  <!-- Franja Vertical -->
  <rect x="0" y="0" width="100" height="200" fill="red" />
  
  <!-- Franja Horizontal -->
  <rect x="0" y="0" width="300" height="50" fill="blue" />
  
  <!-- Intersección -->
  <rect x="0" y="0" width="100" height="50" fill="green" />
</svg>
```

---

## EJERCICIO 2: El Robot Geométrico

### METADATA
- **ID**: EJ-MOD1-002
- **Dificultad**: ⭐⭐ Intermedio
- **Tiempo estimado**: 20 minutos
- **Nivel Bloom**: Crear
- **Conceptos evaluados**: `<circle>`, `<ellipse>`, `<line>`, `<polygon>`.

### ENUNCIADO
Dibuja la cara de un robot usando las siguientes especificaciones exactas:
1. **Cabeza**: Un rectángulo de esquinas redondeadas (rx=15).
2. **Ojos**: Dos círculos perfectos.
3. **Antenas**: Dos líneas que salen de la parte superior de la cabeza.
4. **Boca**: Un polígono triangular invertido.

**Reto Adicional**: Usa medidas relativas o asegúrate que todo esté centrado en un lienzo de 200x200.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
  <!-- Cabeza -->
  <rect x="50" y="50" width="100" height="100" rx="15" fill="#ccc" stroke="black" />
  
  <!-- Ojos -->
  <circle cx="75" cy="80" r="10" fill="white" stroke="black" />
  <circle cx="125" cy="80" r="10" fill="white" stroke="black" />
  
  <!-- Antenas -->
  <line x1="75" y1="50" x2="60" y2="20" stroke="black" stroke-width="2" />
  <line x1="125" y1="50" x2="140" y2="20" stroke="black" stroke-width="2" />
  
  <!-- Boca (Triángulo invertido) -->
  <polygon points="75,120 125,120 100,140" fill="#666" />
</svg>
```

---

## EJERCICIO 3: Debugging de Coordenadas

### METADATA
- **ID**: EJ-MOD1-003
- **Dificultad**: ⭐⭐ Intermedio
- **Tiempo estimado**: 10 minutos
- **Nivel Bloom**: Analizar/Debug
- **Tipo**: Debugging

### ENUNCIADO
El siguiente código intenta dibujar un "blanco de tiro" (círculos concéntricos centrados), pero se ve mal. Encuentra los errores y corrígelos para que estén perfectamente alineados al centro del lienzo 100x100.

```xml
<svg viewBox="0 0 100 100">
  <circle x="50" y="50" r="40" fill="red" />
  <circle cx="50" cy="50" r="30" fill="white" />
  <circle cx="100" cy="100" r="20" fill="red" />
  <rect x="45" y="45" width="10" height="10" fill="black" />
</svg>
```

### SOLUCIÓN Y ANÁLISIS
1. **Error 1**: El primer círculo usa `x, y` en lugar de `cx, cy`. SVG ignora `x, y` en círculos (default a 0), por lo que se dibuja en la esquina.
   - *Corrección*: `<circle cx="50" cy="50" r="40"...>`
2. **Error 2**: El tercer círculo está en `100, 100` (esquina inferior derecha), no en el centro `50, 50`.
   - *Corrección*: `<circle cx="50" cy="50" r="20"...>`
3. **Ajuste Fino**: El rectángulo central (diana) está en `45, 45`. Como es 10x10, su centro será `45+5, 45+5 = 50, 50`. Esto es **correcto**, pero es importante verificarlo.

---

## RÚBRICA GENERAL
- **90-100%**: Código semántico, indentado, usa los atributos correctos (`cx` vs `x`), y cumple visualmente el objetivo.
- **70-89%**: Cumple visualmente pero tiene código desordenado o atributos redundantes.
- **<70%**: Errores de sintaxis XML o uso incorrecto de primitivas (ej. usar 4 líneas para hacer un rectángulo).
