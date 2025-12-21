# EVALUACIÓN: VECTORES VS RASTER

## CUESTIONARIO

### Pregunta 1: Escalabilidad
Si tienes un icono de 100x100 píxeles y lo muestras en una pantalla de 1000x1000 píxeles:

- [ ] a) El JPG se verá mejor que el SVG.
- [ ] b) El SVG recalculará sus curvas y se verá perfectamente nítido.
- [ ] c) Ambos se verán borrosos.

### Pregunta 2: Peso del Archivo
¿Qué determina el peso (KB) de un archivo SVG?

- [ ] a) El tamaño en píxeles (ancho x alto).
- [ ] b) La cantidad de colores usados.
- [ ] c) La complejidad de las formas y la cantidad de instrucciones matemáticas (nodos).

### Pregunta 3: Fotografía
¿Por qué no usamos SVG para guardar fotografías de paisajes?

- [ ] a) Porque SVG no soporta colores.
- [ ] b) Porque tendríamos que dibujar millones de micro-polígonos para simular el realismo, resultando en un archivo pesadísimo e ineficiente.
- [ ] c) Porque los navegadores no soportan fotos.

---

## SOLUCIONARIO

### Pregunta 1: Solución
**Respuesta**: b) El SVG recalculará sus curvas y se verá perfectamente nítido.
**Explicación**: Es la definición de vector. Independiente de la resolución.

### Pregunta 2: Solución
**Respuesta**: c) La complejidad de las formas.
**Explicación**: Un SVG de 10000x10000px que solo contiene un círculo pesa menos que un SVG de 100x100px que contiene un mapa detallado del mundo. Son instrucciones de texto, no mapas de bits.

### Pregunta 3: Solución
**Respuesta**: b) Ineficiencia.
**Explicación**: Para fotos, el mapa de bits es más eficiente con algoritmos de compresión como JPG. Vectorizar una foto crea archivos gigantescos y lentos de procesar.
