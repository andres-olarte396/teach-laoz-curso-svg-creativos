# 🎬 MÓDULO 3: SVG VIVO (ANIMACIÓN)

## 🎯 Objetivo General
Implementar movimiento y respuesta a eventos. Transformarás gráficos estáticos en interfaces vivas que respiran y responden al usuario.

- **Duración estimada**: 1.5 horas
- **Nivel**: Avanzado

---

## 🗺️ Mapa del Módulo

### Tema 3.1: Movimiento
- **[Animación CSS](tema_3.1_subtema_3.1.1_contenido.md)**: Usar `@keyframes` para mover, rotar y cambiar colores.

### Tema 3.2: Respuesta
- **[Interactividad](tema_3.2_subtema_3.2.1_contenido.md)**: Eventos del mouse, `:hover` y un poco de JavaScript.

---

## 🧭 Guía de Estudio Recomendada

### Paso 1: Animación Clásica (45 min)
Ve a **[Animación CSS](tema_3.1_subtema_3.1.1_contenido.md)**. Aprende el truco de `stroke-dasharray`. Es el secreto mejor guardado de los animadores SVG para hacer efectos de "auto-dibujado".
- *Reto*: Haz que u círculo se dibuje a sí mismo.

### Paso 2: Interactividad (45 min)
En **[Interactividad](tema_3.2_subtema_3.2.1_contenido.md)**, concéntrate en la accesibilidad. Un botón bonito que no se puede usar con teclado no sirve.

---

## 💡 Tip del Instructor
Cuidado con animar posiciones (`x`, `y`) directamente. Es mejor animar `transform: translate(x, y)`. Es mucho más suave para el navegador (aceleración por hardware).
