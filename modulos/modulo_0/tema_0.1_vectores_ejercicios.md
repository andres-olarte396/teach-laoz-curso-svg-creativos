# BANCO DE EJERCICIOS: VECTORES VS RASTER

## METADATA
- **Módulo**: 0 (Nivelación)
- **Tema**: Vectores vs Raster

---

## EJERCICIO 1: El Test del Zoom

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: Escalabilidad.

### ENUNCIADO
Abre tu navegador. Busca el logo de Google en Imágenes (formato PNG) y abre una nueva pestaña con un icono SVG cualquiera.
Aplica zoom al 500% (Ctrl + +).
Describe qué le pasa a los bordes de cada uno.

### SOLUCIÓN MODELO
- **PNG**: Los bordes se ven como escaleras ("dientes de sierra"). Se notan los cuadros de color.
- **SVG**: La línea curva sigue siendo perfectamente suave, sin importar cuánto me acerque.

---

## EJERCICIO 2: Decisión de Formato

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: Casos de uso.

### ENUNCIADO
Eres el líder técnico de un proyecto web. Debes decidir el formato para las siguientes imágenes. ¿SVG o JPG?
1. La foto de perfil del usuario (una fotografía de su cara).
2. El icono del menú (tres rayas horizontales).
3. Un gráfico estadístico de barras que debe ser interactivo.
4. El logo de la empresa que va en el pie de página.

### SOLUCIÓN MODELO
1. **JPG/WebP**: Es una fotografía compleja con millones de colores. Vectorizarla sería ineficiente.
2. **SVG**: Geometría simple, necesita ser nítido.
3. **SVG**: Necesita ser interactivo (DOM) y nítido.
4. **SVG**: Es un logo, geometría pura.
