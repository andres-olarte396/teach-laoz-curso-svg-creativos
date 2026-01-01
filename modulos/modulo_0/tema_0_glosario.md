# GLOSARIO TÉCNICO: CREACIÓN DE SVGS CREATIVOS

## A

**Attribute (Atributo)**: Propiedad definida dentro de la etiqueta de apertura de un elemento SVG (ej: `width="100"`, `fill="red"`). Controlan la apariencia y geometría.

## B

**Bézier Curve (Curva de Bézier)**: Fórmula matemática usada para dibujar curvas suaves escalables. Se definen por puntos de anclaje (inicio/fin) y puntos de control (que "tiran" de la curva).

## C

**Coordinate System (Sistema de Coordenadas)**: El espacio infinito 2D donde se dibujan los elementos SVG. Por defecto, 1 unidad = 1 pixel.

## D

**Defs (Definiciones)**: Elemento `<defs>` usado para definir objetos (gradientes, patrones, formas) que no se renderizan inmediatamente, sino que se almacenan para ser usados después.
**DOM (Document Object Model)**: La estructura de árbol que representa el documento SVG/HTML. Permite que JavaScript acceda y modifique cada elemento (círculo, path, grupo) individualmente.

## G

**Gradient (Gradiente)**: Transición suave entre dos o más colores. Puede ser Lineal (a lo largo de una recta) o Radial (desde un punto central).
**Group (Grupo)**: Elemento `<g>` que actúa como contenedor lógico. Permite transformar y aplicar estilos a múltiples objetos hijos simultáneamente.

## F

**Fill (Relleno)**: El color, gradiente o patrón que llena el interior de una forma vectorial.

## K

**Keyframes**: Regla CSS (`@keyframes`) que define los estados intermedios de una animación en puntos específicos del tiempo (ej: al 0% y al 100%).

## M

**Mask (Máscara)**: Herramienta de ocultación basada en luminancia (blanco/negro). Permite transparencias graduales y bordes difuminados, a diferencia del recorte duro (`cliPath`).

## P

**Path (Trazado)**: La primitiva SVG más potente (`<path>`). Permite dibujar cualquier forma arbitraria mediante una secuencia de comandos (M, L, C, Z).

## S

**Stroke (Trazo)**: La línea que bordea una forma SVG. Tiene propiedades como ancho (`stroke-width`), color (`stroke`) y estilo de línea (`stroke-dasharray`).
**Symbol (Símbolo)**: Elemento similar a un grupo pero con su propio `viewBox` y sistema de coordenadas interno. Ideal para crear plantillas de iconos reutilizables.

## T

**Transform (Transformación)**: Atributo que modifica el sistema de coordenadas de un elemento para moverlo (`translate`), rotarlo (`rotate`), escalarlo (`scale`) o inclinarlo (`skew`).

## V

**Vector**: Imagen generada matemáticamente, independiente de la resolución.
**ViewBox**: Atributo mágico del elemento `<svg>` que define la ventana visible y el sistema de coordenadas interno, permitiendo que el gráfico sea "responsive".
