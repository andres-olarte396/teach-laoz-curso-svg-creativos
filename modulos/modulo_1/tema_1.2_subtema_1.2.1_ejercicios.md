# BANCO DE EJERCICIOS: COMANDOS LINEALES (PATH)

## METADATA
- **Módulo**: Primitivas y Trazados
- **Tiempo total estimado**: 30 minutos
- **Nivel de ruta**: Intermedia

---

## EJERCICIO 1: El Decodificador Humano

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: Interpretación de `d`.

### ENUNCIADO
Sin usar el ordenador (papel y lápiz), dibuja la forma que describe este path en un grid de 10x10.
`d="M 1 1 H 9 V 9 H 1 Z"`

¿Qué forma es?
- a) Un círculo
- b) Un triángulo
- c) Un cuadrado
- d) Una línea recta

### SOLUCIÓN
**c) Un cuadrado.**
1. Mueve a 1,1 (Esquina sup izq)
2. H 9 (Línea horizontal hasta X=9) -> Borde superior
3. V 9 (Línea vertical hasta Y=9) -> Borde derecho
4. H 1 (Línea horizontal hasta X=1) -> Borde inferior
5. Z (Cierra vuelta a 1,1) -> Borde izquierdo

---

## EJERCICIO 2: Tu Inicial Pixelada

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `M`, `L`, `H`, `V`.

### ENUNCIADO
Dibuja la primera letra de tu nombre usando solo líneas rectas y ángulos de 90 grados (estilo pixel art o bloque).
Debes usar al menos un comando `H` y un comando `V` para simplificar tu código.
Lienzo: 100x100.

**Ejemplo (Letra L)**:
`<path d="M 20 20 V 80 H 60 L 60 70 H 30 V 20 Z" />`

---

## EJERCICIO 3: Traductor Relativo

### ENUNCIADO
Convierte el siguiente path absoluto a relativo.
Absoluto: `M 10 10 L 20 10 L 20 20 L 10 20 Z`

Tu respuesta debe empezar con `m 10 10 ...` y usar letras minúsculas (`l`, `h`, `v` o `z`).

### SOLUCIÓN
`d="m 10 10 l 10 0 l 0 10 l -10 0 z"`
O más optimizado usando H y V:
`d="m 10 10 h 10 v 10 h -10 z"`

Nota: `z` (minúscula) y `Z` (mayúscula) hacen lo mismo, cierran el path.
