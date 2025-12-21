# BANCO DE EJERCICIOS: PLANIFICACIÓN Y DISEÑO

## METADATA
- **Módulo**: Proyecto Final
- **Tiempo total estimado**: 30 minutos
- **Nivel de ruta**: Experto

---

## EJERCICIO 1: Decomposición de la Nave Espacial

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: Pensamiento primitivo, desglose de formas.

### ENUNCIADO
Mira un objeto complejo a tu alrededor (ej. tu mouse, una taza, una lámpara).
No lo dibujes. Escribe en un papel (o archivo de texto) un "Pseudocódigo SVG" de cómo lo construirías.
Ejemplo para una taza:
- `defs`:
  - `gradient-cafe`: linearGradient (marron oscuro -> marron claro)
- `g id="taza"`:
  - `rect`: cuerpo principal (rounded corners)
  - `path`: asa (curva bezier C)
  - `ellipse`: superficie del liquido (fill url(#gradient-cafe))

Haz lo mismo para una **Nave Espacial Retro**.
Define al menos 3 componentes principales y qué primitivas usarías (`rect`, `circle`, `path`).

### SOLUCIÓN MODELO
*N/A - Es un ejercicio conceptual. Se busca que el alumno identifique partes.*
Ejemplo de respuesta válida:
**Nave Espacial:**
1. **Cuerpo**: `ellipse` vertical alargada.
2. **Aletas**: 2 `path` triangulares a los lados.
3. **Ventana**: `circle` con borde grueso.
4. **Fuego**: `path` animado en la base.

---

## EJERCICIO 2: Arquitectura de Archivos

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `<defs>`, `<symbol>`, IDs.

### ENUNCIADO
Vas a crear un sistema solar.
Escribe SOLO la estructura `<defs>` necesaria para tener:
1. Una plantilla de Planeta (`<symbol>` con un círculo).
2. Tres gradientes diferentes para planetas: "Tierra" (Azul/Verde), "Marte" (Rojo/Naranja), "Júpiter" (Beige/Marrón).
3. Un ID consistente para cada recurso.

No dibujes los planetas aún (no uses `<use>`), solo prepara el almacén.

### SOLUCIÓN MODELO
```xml
<defs>
  <!-- Plantilla Geométrica -->
  <symbol id="template-planet" viewBox="0 0 100 100">
    <circle cx="50" cy="50" r="50" />
  </symbol>

  <!-- Paletas de Colores (Estilos) -->
  <radialGradient id="grad-earth">
    <stop offset="0%" stop-color="blue" />
    <stop offset="100%" stop-color="green" />
  </radialGradient>

  <radialGradient id="grad-mars">
    <stop offset="0%" stop-color="orange" />
    <stop offset="100%" stop-color="red" />
  </radialGradient>

  <radialGradient id="grad-jupiter">
    <stop offset="0%" stop-color="#ddccaa" />
    <stop offset="100%" stop-color="#886644" />
  </radialGradient>
</defs>
```

---

## EJERCICIO 3: El Boceto de Coordenadas

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `viebox`, `transform`, planificación espacial.

### ENUNCIADO
Tienes un lienzo de `800x600`.
Quieres colocar 4 tarjetas de información (widgets) de `150x200` cada una.
Calcula mentalmente las coordenadas `x, y` para distribuir estas tarjetas equitativamente en el centro, dejando espacio entre ellas.
Escribe los comandos `<use href="#card" x="?" y="?" />` necesarios.
Asume que el punto de anclaje de la tarjeta es su esquina superior izquierda (0,0).

### SOLUCIÓN MODELO
*Cálculo aproximado:*
Espacio total X: 800.
Tarjetas: 4 * 150 = 600px ocupados.
Espacio libre X: 800 - 600 = 200px.
Huecos: 5 huecos (bordes + entre tarjetas) -> 200 / 5 = 40px por hueco.
Y centrado: (600 - 200) / 2 = 200px.

```xml
<use href="#card" x="40" y="200" />
<use href="#card" x="230" y="200" /> <!-- 40 + 150 + 40 -->
<use href="#card" x="420" y="200" /> <!-- 230 + 150 + 40 -->
<use href="#card" x="610" y="200" /> <!-- 420 + 150 + 40 -->
```
