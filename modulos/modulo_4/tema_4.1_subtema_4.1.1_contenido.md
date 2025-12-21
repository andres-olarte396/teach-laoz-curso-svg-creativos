# RECURSO VISUAL: ILUSTRACIÓN DEL TEMA

![Ilustración Subtema 4.1.1](../../media/ilustraciones/ilustracion_subtema_4.1.1.svg)

# PROYECTO FINAL: PLANIFICACIÓN Y DISEÑO

**Tiempo estimado**: 60 minutos
**Nivel**: Experto
**Prerrequisitos**: Módulos 1, 2 y 3 Completos

## ¿Por qué importa este concepto?
Saber escribir `<circle>` o `@keyframes` por separado está bien. Pero la ingeniería de software real (y el arte digital real) consiste en **combinar** estas piezas para construir un sistema complejo.
En este módulo, no aprenderemos etiquetas nuevas. Aprenderemos a **pensar** en SVG.
Cómo estructurar un archivo grande, cómo nombrar las cosas para no volverse loco, y cómo planear una animación compleja antes de escribir una sola línea de código.

## El Desafío: "La Infografía del Clima Espacial"
Construiremos un widget del clima interactivo para una base en Marte.
**Requerimientos:**
1.  **Iconos Reutilizables**: Sol, Nubes, Lluvia (usando `<defs>`).
2.  **Ambiente**: Fondo con gradiente (Módulo 2).
3.  **Estado**: Un indicador que cambie de color (Módulo 3 - CSS).
4.  **Interactividad**: Al hacer clic en un botón, cambia el clima (Módulo 3 - JS).

---

## Comprensión intuitiva: Arquitectura SVG
Un SVG profesional se parece más a una aplicación que a una imagen.
Tiene capas:
1.  **Capa de Recursos (`defs`)**: Donde viven los actores antes de salir a escena.
2.  **Capa de Estructura (`g`)**: Agrupamos elementos lógicos (Fondo, UI, Contenido).
3.  **Capa de Lógica (`script/style`)**: El cerebro y el maquillaje.

---

## Paso 1: Boceto y Descomposición
Antes de tocar el teclado, dibuja (en papel o mentalmente).
Desglosa tu visión en **Primitivas**:
- "¿La nube?" -> Son 3 círculos superpuestos y un rectángulo base.
- "¿El sol?" -> Un círculo central y rayos (líneas rotadas).
- "¿El botón?" -> Un rectángulo con esquinas redondeadas (`rx`) y texto.

## Paso 2: Estrategia de Namespaces (IDs)
En un proyecto grande, `id="circulo"` es pecado mortal.
Usa una convención: `componente-elemento-estado`.
- `weather-icon-sun`
- `ui-button-toggle`
- `bg-gradient-mars`

---

## Implementación práctica: El Esqueleto

```xml
<svg viewBox="0 0 400 300" xmlns="http://www.w3.org/2000/svg">
  <!-- 1. DEFINICIONES (La Biblioteca) -->
  <defs>
    <!-- Gradiente del cielo marciano -->
    <linearGradient id="bg-mars" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#ff9966" />
      <stop offset="100%" stop-color="#cc3300" />
    </linearGradient>

    <!-- Icono: Nube (Componente reutilizable) -->
    <symbol id="icon-cloud" viewBox="0 0 100 60">
      <circle cx="30" cy="30" r="20" fill="white" />
      <circle cx="70" cy="30" r="20" fill="white" />
      <circle cx="50" cy="20" r="25" fill="white" />
      <rect x="30" y="30" width="40" height="20" fill="white" />
    </symbol>
  </defs>

  <!-- 2. ESTRUCTURA (El Escenario) -->
  
  <!-- Fondo Base -->
  <rect id="background" width="100%" height="100%" fill="url(#bg-mars)" />

  <!-- Contenedor Principal del Widget -->
  <g id="widget-container" transform="translate(50, 50)">
    <!-- Aquí irán nuestros iconos instanciados con <use> -->
  </g>

  <!-- Zona de Interfaz (UI) -->
  <g id="ui-controls" transform="translate(150, 250)">
    <!-- Aquí irá el botón -->
  </g>

</svg>
```

---

## Errores frecuentes en Proyectos Grandes

### ❌ Error 1: Coordenadas Mágicas
Escribir `M 342 593` es difícil de mantener.
**Solución**: Usa `transform="translate(x,y)"` en grupos (`<g>`) para mover conjuntos enteros. Diseña tus iconos en `0,0` y muévelos después.

### ❌ Error 2: CSS Global
Poner `circle { fill: red; }` en tu CSS afectará a TODOS los círculos, incluso los que no querías.
**Solución**: Usa clases semánticas. `.icon-status { fill: red; }`.

---

## Resumen del concepto

**En una frase**: Un proyecto SVG profesional requiere planificación: define recursos primero, agrupa lógicamente después, y usa nombres consistentes.

**Cuándo usarlo**: Siempre que hagas algo más complejo que un icono simple.

**Siguiente paso**: Tenemos el plano. Ahora vamos a construir la casa. En el siguiente tema, escribiremos el código final, las animaciones y el JavaScript.



## 🕹️ LABORATORIO VIRTUAL

> [!TIP]
> **Experiencia Práctica**: Preview: Objetivo Final (Widget)
> 
> [Abrir Simulación](../../recursos/simulaciones/sim_4.1_weather_preview.html)

