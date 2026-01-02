# EVALUACIÓN: CURVAS DE BÉZIER

## CUESTIONARIO

### Pregunta 1: C vs Q

¿Cuántos pares de coordenadas (puntos) necesitas especificar después del comando `C` (Cúbica)?

- a) 1 (Destino)
- b) 2 (Control + Destino)
- c) 3 (Control1 + Control2 + Destino)

### Pregunta 2: Curvas Suaves

Para hacer una curva con forma de "S" perfecta en un solo comando, ¿cuál primitiva DEBES usar?

- a) `L` (Line)
- b) `Q` (Quadratic)
- c) `C` (Cubic)

### Pregunta 3: El Atajo T

¿Qué hace el comando `T`?

- a) Termina el path.
- b) Crea una curva Cuadrática asumiendo el punto de control reflejado del anterior.
- c) Crea texto en el path.

---

## SOLUCIONARIO

### Pregunta 1: Solución

**Respuesta**: c) 3.
**Justificación**: La curva cúbica necesita 2 puntos de control y 1 punto final. Total 3 pares de coordenadas (6 números). `Q` necesita 2 pares.

### Pregunta 2: Solución

**Respuesta**: c) `C` (Cubic).
**Justificación**: La curva Cuadrática (`Q`) al tener solo un punto de control, solo puede curvarse en una dirección (como un arco). Solo la Cúbica (`C`) con dos controles puede tirar en direcciones opuestas para formar una "S".

### Pregunta 3: Solución

**Respuesta**: b) Crea una curva Cuadrática suave.
**Justificación**: `T` es el atajo para "Smooth Quadratic". Usa el reflejo del punto de control previo para asegurar tangencia continua (suavidad).
