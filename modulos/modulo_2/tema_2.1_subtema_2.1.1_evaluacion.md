# EVALUACIÓN: DEFINICIONES Y REUTILIZACIÓN

## CUESTIONARIO

### Pregunta 1: Invisibilidad
Si coloco un `<circle>` dentro de una etiqueta `<defs>`, ¿qué se ve en la pantalla por defecto?

- [ ] a) Un círculo negro.
- [ ] b) Nada.
- [ ] c) Un círculo transparente.

### Pregunta 2: El Clonador
¿Qué atributo se usa en `<use>` para seleccionar qué elemento vamos a clonar?

- [ ] a) `src`
- [ ] b) `id`
- [ ] c) `href`

### Pregunta 3: Dominancia de Estilo
Tienes un original: `<circle id="c" fill="red" />`.
Haces un uso: `<use href="#c" fill="blue" />`.
¿De qué color sale el clon?

- [ ] a) Azul, porque el uso sobrescribe.
- [ ] b) Rojo, porque el original tiene un estilo explícito que gana por especificidad.
- [ ] c) Morado, se mezclan.

---

## SOLUCIONARIO

### Pregunta 1: Solución
**Respuesta**: b) Nada.
**Explicación**: El elemento `<defs>` está diseñado específicamente para definir recursos sin renderizarlos. Es almacenamiento puro.

### Pregunta 2: Solución
**Respuesta**: c) `href`.
**Explicación**: La sintaxis moderna es `href="#id"`. Antiguamente se usaba `xlink:href`, pero ya no es necesario (aunque SVG es retrocompatible).

### Pregunta 3: Solución
**Respuesta**: b) Rojo.
**Explicación**: En el modelo de herencia SVG/CSS, el estilo definido directamente en el elemento original tiene mayor precedencia que el estilo heredado desde el elemento `<use>`. Para que fuera azul, el original no debería tener atributo `fill` (o tenerlo como `currentColor`).
