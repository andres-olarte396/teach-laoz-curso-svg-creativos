# GUIÓN: DEFINICIONES Y REUTILIZACIÓN

## FICHA TÉCNICA
- **Duración**: 4 minutos
- **Tono**: Eficiente y profesional.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**:
En programación existe un mantra sagrado: DRY. Don't Repeat Yourself. No te repitas.
Si estás dibujando un bosque, sería una locura escribir el código de un árbol y luego copiarlo y pegarlo cien veces. ¿Y si luego quieres cambiar el color de las hojas? Tendrías que editar cien copias.
SVG tiene la solución elegante a este problema: Las Definiciones y el Uso.

---

### 00:45 - EL CAMERINO (DEFS)

**[LOCUTOR]**:
El elemento `<defs>` es como un camerino detrás del escenario. Todo lo que dibujas ahí adentro es invisible. Existe matemáticamente, pero no se renderiza en la pantalla final.
Es el lugar perfecto para guardar tus "originales", tus plantillas.
Les pones un ID único, como "mi-arbol", y los dejas ahí, listos para salir a escena.

---

### 01:30 - SALIENDO A ESCENA (USE)

**[LOCUTOR]**:
Para mostrar ese árbol, usamos el elemento `<use>`.
`<use href="#mi-arbol" />`.
Es como crear un holograma o un clon de la plantilla original.
Puedes colocar este clon donde quieras con `x` e `y`. Puedes rotarlo, escalarlo, cambiarle la opacidad.
Y aquí viene lo mejor: Si vas al camerino (`defs`) y cambias el árbol original a color rojo, ¡todos los clones en el escenario se volverán rojos instantáneamente!

---

### 02:30 - SYMBOL VS GROUP

**[LOCUTOR]**:
Un consejo pro: Si vas a crear iconos, en lugar de usar grupos (`<g>`) dentro de las definiciones, usa `<symbol>`.
El símbolo te permite definir su propia caja de coordenadas independiente (`viewBox`), lo que hace que cambiarles el tamaño después sea muchísimo más fácil.

---

### 03:15 - CONCLUSIÓN

**[LOCUTOR]**:
Así que recuerda: Dibuja una vez, úsalo infinitas veces.
Tu archivo pesará menos y tu yo del futuro te agradecerá cuando tenga que hacer cambios.
Ahora, ¡vamos a clonar!
