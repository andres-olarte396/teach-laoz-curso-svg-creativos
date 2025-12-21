# MÓDULO 0: DIAGNÓSTICO Y NIVELACIÓN - LECCIÓN INTRODUCTORIA

## ¡Bienvenido al Curso de SVGs Creativos!

Antes de sumergirnos en el código, es fundamental que domines estos conceptos base. Considéralos los cimientos de tu rascacielos visual.

---

## 1. Gráficos Vectoriales vs. Mapa de Bits

### Definición
Los gráficos vectoriales (como SVG) se definen mediante fórmulas matemáticas (líneas, curvas, formas), mientras que los mapas de bits (JPG, PNG) son una cuadrícula de píxeles fijos.

### ¿Por qué es fundamental?
Imagina una banda elástica vs. una foto impresa. Si estiras la banda (vector), mantiene su forma y nitidez. Si estiras la foto (raster), se ve borrosa ("pixeleada"). En la web moderna, necesitamos "bandas elásticas" que se vean perfectas en un reloj inteligente y en una pantalla 4K.

### Importancia: 10/10
Sin entender esto, tratarás el SVG como una imagen estática y perderás todos sus superpoderes (escalabilidad, animación, interactividad).

---

## 2. XML (eXtensible Markup Language)

### Definición
SVG es un dialecto de XML. Es un lenguaje de marcado estricto que usa etiquetas (`<tag>`) para definir objetos.

### ¿Por qué es fundamental?
Si sabes HTML, ya sabes el 80% de la sintaxis. Pero XML es más estricto: todas las etiquetas deben cerrarse, los atributos deben tener comillas, y es sensible a mayúsculas/minúsculas. Un error de sintaxis aquí no solo "se ve mal", sino que puede romper todo el gráfico.

### Importancia: 9/10

---

## 3. El Sistema de Coordenadas Cartesiano (El "Lienzo")

### Definición
En la web (y en SVG), el origen `(0,0)` está en la **esquina superior izquierda**.
- **X aumenta** hacia la derecha along.
- **Y aumenta** hacia abajo (al revés que en las matemáticas tradicionales del colegio).

### ¿Por qué es fundamental?
Es tu mapa. Si le dices al ordenador "dibuja un círculo en 50,50", necesitas saber exactamente dónde caerá. Entender que `Y` positivo es "hacia abajo" es el error #1 de los principiantes.

### Importancia: 10/10

---

## 4. El DOM (Document Object Model)

### Definición
Cada forma que dibujas en SVG (un círculo, un rectángulo) se convierte en un nodo en el árbol del documento, exactamente igual que un `<div>` o un `<p>`.

### ¿Por qué es fundamental?
Significa que puedes usar CSS para cambiar su color (`fill: red`) y JavaScript para moverlo (`element.setAttribute('x', 100)`). El SVG no es una "caja negra"; es parte viva de tu página web.

### Importancia: 8/10
