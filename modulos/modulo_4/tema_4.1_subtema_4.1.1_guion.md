# GUIÓN: PLANIFICACIÓN Y DISEÑO (PROYECTO FINAL)

## FICHA TÉCNICA
- **Duración**: 4-5 minutos
- **Tono**: Estratégico y reflexivo.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**:
Bienvenido al Módulo 4. La recta final.
Aquí es donde dejamos de ser aprendices de comandos y nos convertimos en arquitectos de SVG.
Vamos a construir un proyecto completo: Un Widget de Clima Espacial para Marte.
Pero antes de escribir una sola línea de código, vamos a hacer algo más importante: Vamos a pensar.

---

### 00:45 - LA REGLA DEL 80/20

**[LOCUTOR]**:
En el desarrollo profesional, el 80% del éxito está en la planificación.
Si empiezas a escribir código a lo loco, acabarás con un archivo espagueti imposible de mantener.
¿Cuál es nuestro plan?
1. Descomponer la visión en primitivas. ¿Qué formas básicas veo?
2. Definir los recursos reutilizables. ¿Qué se repite? (Esas nubes van a `defs`).
3. Establecer una paleta de nombres. Nada de `<g id="g1">`. Usaremos nombres semánticos como `cloud-icon` o `ui-container`.

---

### 01:30 - EL CANVAS MENTAL

**[LOCUTOR]**:
Imagina tu lienzo de 400x300.
Divide el espacio mentalmente.
"Arriba a la izquierda pondré el sol. Abajo el texto de temperatura. En el fondo, un gradiente".
Si haces este mapa mental ahora, no tendrás que estar probando números aleatorios en `x` e `y` durante horas.

---

### 02:15 - PREPARANDO EL ENTORNO

**[LOCUTOR]**:
Nuestra estructura será limpia:
- Un bloque `<defs>` arriba para gradientes y símbolos.
- Un bloque de estilos CSS (`<style>`) para las animaciones.
- Un cuerpo principal (`<g>`) organizado por capas. Fondo primero, contenido después, interfaz de usuario al final.

---

### 03:00 - MANOS A LA OBRA

**[LOCUTOR]**:
Toma un papel y un lápiz. Sí, analógico.
Dibuja tu widget. Haz flechas. Pon nombres a las partes.
Ese papel es tu plano de arquitectura.
Una vez que lo tengas, nos vemos en la siguiente lección para empezar la construcción.
