# BANCO DE EJERCICIOS: IMPLEMENTACIÓN Y REFINAMIENTO

## METADATA
- **Módulo**: Proyecto Final
- **Tiempo total estimado**: 90 minutos
- **Nivel de ruta**: Experto

---

## EJERCICIO 1: Debugging Visual

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `viewBox`, `clipping`, `overflow`.

### ENUNCIADO
Tienes un SVG de `100x100`. Dentro dibujas un círculo en `cx="100" cy="100" r="50"`.
Visualmente aparece cortado (solo se ve un cuarto de círculo en la esquina inferior derecha).
Sin mover el círculo (`cx, cy`), ¿cómo modificas el elemento raíz `<svg>` para que el círculo se vea completo y centrado en el lienzo?

### SOLUCIÓN MODELO
Cambiar el `viewBox`.
Si el círculo está en `100,100` y tiene radio `50`, ocupa desde `x=50` hasta `x=150`, y `y=50` hasta `y=150`.
Para verlo centrado y completo, el `viewBox` debe capturar esa área.
`<svg viewBox="50 50 100 100" ...>`
(Origen 50,50, Ancho 100, Alto 100).

---

## EJERCICIO 2: La Tarjeta de Perfil (Integración)

### METADATA
- **Dificultad**: ⭐⭐⭐ Avanzado
- **Conceptos evaluados**: Proyecto completo mini.

### ENUNCIADO
Crea un archivo `tarjeta.svg` que contenga:
1.  **Fondo**: Rectángulo con bordes redondeados y sombra (avanzado: usa `filter` o simula sombra con otro rect gris desplazado).
2.  **Avatar**: Círculo con una imagen (o color sólido) recortada por un `clipPath` circular.
3.  **Nombre**: Texto centrado.
4.  **Botón "Seguir"**: Que cambie de color al pasar el mouse (CSS) y muestre un alert "Siguiendo..." al hacer clic (JS).

### SOLUCIÓN MODELO
*Ver código similar en el contenido del tema. Se evalúa la estructura limpia `<defs>`, `<style>` y la funcionalidad de JS.*

---

## EJERCICIO 3: Accesibilidad

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: `title`, `desc`, `role`.

### ENUNCIADO
Tienes un SVG que es un gráfico de ventas complejo.
Un usuario ciego usa un lector de pantalla. Actualmente, el lector no dice nada o dice "imagen".
Añade las etiquetas necesarias para que el lector diga: "Gráfico de barras mostrando ventas de 2024. Enero fue el mejor mes".

### SOLUCIÓN MODELO
```xml
<svg aria-labelledby="titulo desc" role="img">
  <title id="titulo">Gráfico de Ventas 2024</title>
  <desc id="desc">Gráfico de barras donde se observa que Enero tuvo el pico más alto...</desc>
  <!-- Resto del gráfico -->
</svg>
```
