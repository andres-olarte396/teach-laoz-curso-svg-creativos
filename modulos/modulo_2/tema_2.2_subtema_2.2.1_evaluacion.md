# EVALUACIÓN: MÁSCARAS Y RECORTES

## CUESTIONARIO

### Pregunta 1: Rojo vs Negro

Estás definiendo una `mask` (máscara de luminancia).
Pintas un círculo ROJO puro (`#FF0000`). ¿Cómo afecta a la visibilidad?

- [ ] a) Lo hace rojo.
- [ ] b) Es invisible (como el negro).
- [ ] c) Es parcialmente visible (basado en cuán "claro" es el color rojo).

### Pregunta 2: Bordes Suaves

¿Qué herramienta DEBES usar si quieres que los bordes de tu imagen se difuminen suavemente hasta desaparecer?

- [ ] a) `<clipPath>`
- [ ] b) `<mask>`
- [ ] c) `<filter>`

### Pregunta 3: El Atributo de Unión

¿Qué atributo pones en el elemento que quieres recortar para aplicarle un clipPath definido con `id="corte"`?

- [ ] a) `clip-path="url(#corte)"`
- [ ] b) `clip="corte"`
- [ ] c) `path="url(#corte)"`

---

## SOLUCIONARIO

### Pregunta 1: Solución

**Respuesta**: c) Es parcialmente visible.
**Justificación**: Las máscaras de luminancia calculan el brillo del color. El rojo puro tiene cierto brillo (no es negro ni blanco), por lo que resultará en una semitransparencia grisácea.

### Pregunta 2: Solución

**Respuesta**: b) `<mask>`.
**Justificación**: El `clipPath` es vector puro, no soporta antialiasing ni gradientes de opacidad (excepto el suavizado de borde básico del navegador). Solo la `mask` con gradientes permite difuminados.

### Pregunta 3: Solución

**Respuesta**: a) `clip-path="url(#corte)"`.
**Justificación**: Es la sintaxis estándar CSS/SVG. Se usa `url(#id)` como referencia funcional.
