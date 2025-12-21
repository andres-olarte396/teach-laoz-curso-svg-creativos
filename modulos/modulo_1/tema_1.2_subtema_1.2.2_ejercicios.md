# BANCO DE EJERCICIOS: CURVAS DE BÉZIER

## METADATA
- **Módulo**: Primitivas y Trazados
- **Tiempo total estimado**: 60 minutos
- **Nivel de ruta**: Avanzada

---

## EJERCICIO 1: La Gota de Agua (Cuadrática)

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `Q`, simetría.

### ENUNCIADO
Dibuja una forma de gota de agua o lágrima usando solo 2 curvas cuadráticas (`Q`).
- Inicio: `(100, 20)` (Punta superior).
- Base redondeada: `(100, 150)`.
- Puntos de control sugeridos: `(20, 100)` y `(180, 100)`.

Cierra la forma con `Z`.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 200">
  <!-- Lado izquierdo: De punta a base, jalado hacia la izquierda -->
  <!-- Lado derecho: De base a punta, jalado hacia la derecha -->
  <path d="M 100 20 Q 20 100 100 150 Q 180 100 100 20 Z" 
        fill="cyan" stroke="blue" />
</svg>
```

---

## EJERCICIO 2: El Corazón (Cúbica)

### METADATA
- **Dificultad**: ⭐⭐⭐ Avanzado
- **Conceptos evaluados**: `C`.

### ENUNCIADO
Un corazón clásico se compone de dos curvas cúbicas principales unidas en la punta inferior y el valle superior.
Dibuja un corazón centrado.
Pista:
- Inicio (Valle superior): `(100, 40)`
- Punta inferior: `(100, 160)`
- Usa `C` para inflar los lóbulos hacia arriba y afuera.

### SOLUCIÓN MODELO
```xml
<path d="M 100 40 
         C 100 0 20 0 20 60 
         C 20 110 80 140 100 160 
         C 120 140 180 110 180 60 
         C 180 0 100 0 100 40 Z" 
      fill="red" />
```
*(Nota: Esta es una versión simplificada de 4 curvas para mayor control, aunque se puede hacer con 2).*

---

## EJERCICIO 3: Diagnóstico de Picos

### ENUNCIADO
Tienes dos curvas conectadas:
`M 0 50 Q 50 0 100 50 Q 50 100 200 50`

En el punto de unión `(100, 50)`, hay un pico visible (una esquina afilada), no una onda suave.
¿Por qué? Dibuja los vectores de control mentalmente.

### SOLUCIÓN
**Análisis**:
- La primera curva `Q 50 0 100 50` llega al punto `100, 50` "viniendo desde arriba" (su tangente final apunta hacia `100,50` desde `50,0`).
- La segunda curva `Q 50 100 200 50` sale de `100, 50` "yendo hacia abajo" (su tangente inicial apunta hacia `50,100`).
- Como las tangentes no son colineales (forman un ángulo agudo), se crea una esquina. Para que fuera suave, el segundo punto de control debería estar opuesto al primero (ej. `150, 100`).
