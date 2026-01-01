# EVALUACIÓN: VECTORES VS RASTER

## CUESTIONARIO

### Pregunta 1: Escalabilidad

Si tienes un icono de 100x100 píxeles y lo muestras en una pantalla de 1000x1000 píxeles:

- a) El JPG se verá mejor que el SVG.
- b) El SVG recalculará sus curvas y se verá perfectamente nítido. (Correcta)
- c) Ambos se verán borrosos.

### Pregunta 2: Peso del Archivo

¿Qué determina el peso (KB) de un archivo SVG?

- a) El tamaño en píxeles (ancho x alto).
- b) La cantidad de colores usados.
- c) La complejidad de las formas y la cantidad de instrucciones matemáticas (nodos). (Correcta)

### Pregunta 3: Fotografía

¿Por qué no usamos SVG para guardar fotografías de paisajes?

- a) Porque SVG no soporta colores.
- b) Porque tendríamos que dibujar millones de micro-polígonos para simular el realismo, resultando en un archivo pesadísimo e ineficiente. (Correcta)
- c) Porque los navegadores no soportan fotos.

---

## SOLUCIONARIO

### Respuesta 1: **b)**

> **Justificación**: Exacto. Al ser gráficos definidos por ecuaciones matemáticas (vectores), los SVG pueden redimensionarse a cualquier tamaño sin perder nitidez ni pixelarse.

### Respuesta 2: **c)**

> **Justificación**: Correcto. El tamaño en píxeles no afecta el peso del archivo SVG; lo que importa es la cantidad de elementos vectoriales, nodos y la complejidad de las curvas matemáticas.

### Respuesta 3: **b)**

> **Justificación**: Así es. Las fotografías contienen millones de variaciones de color y tono pixel a pixel. Intentar replicar eso con vectores requeriría millones de formas geométricas, generando un archivo extremadamente pesado y difícil de procesar.
