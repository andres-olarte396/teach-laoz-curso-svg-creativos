# BANCO DE EJERCICIOS: DEFINICIONES Y REUTILIZACIÓN

## METADATA
- **Módulo**: Estilizado Avanzado y Efectos
- **Tiempo total estimado**: 40 minutos
- **Nivel de ruta**: Intermedia

---

## EJERCICIO 1: El Cielo Estrellado

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: `<defs>`, `<use>`.

### ENUNCIADO
Dibuja un cielo nocturno (rectángulo negro).
Define una sola estrella (forma simple o círculo blanco pequeño) en `<defs>`.
Usa `<use>` para colocar al menos 5 estrellas en diferentes posiciones del cielo.
Juega con el atributo `opacity` en algunas instancias para que brillen diferente.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 200">
  <defs>
    <circle id="star" r="2" fill="white" />
  </defs>
  
  <rect width="200" height="200" fill="#000033" />
  
  <use href="#star" x="20" y="30" />
  <use href="#star" x="50" y="80" opacity="0.5" />
  <use href="#star" x="150" y="40" transform="scale(1.5)" />
  <use href="#star" x="120" y="120" />
  <use href="#star" x="180" y="180" opacity="0.8" />
</svg>
```

---

## EJERCICIO 2: El Ejército de Clones (Colores dinámicos)

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: Herencia de estilos en `<use>`.

### ENUNCIADO
Define un "soldado" (un círculo y un pequeño rectángulo) en `<defs>`.
**IMPORTANTE**: No le pongas color de relleno (`fill`) en la definición.
Luego crea 3 instancias (`<use>`):
1. Un ejército rojo.
2. Un ejército azul.
3. Un ejército verde.
Demuestra que puedes colorear la instancia desde fuera.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 100">
  <defs>
    <g id="soldado"> <!-- Sin fill aquí -->
      <circle cx="0" cy="0" r="10" />
      <rect x="-10" y="10" width="20" height="20" />
    </g>
  </defs>
  
  <use href="#soldado" x="30" y="30" fill="red" />
  <use href="#soldado" x="80" y="30" fill="blue" />
  <use href="#soldado" x="130" y="30" fill="green" />
</svg>
```

---

## EJERCICIO 3: El Icono Escalable (Symbol)

### METADATA
- **Dificultad**: ⭐⭐⭐ Avanzado
- **Conceptos evaluados**: `<symbol>`, `viewBox` independiente.

### ENUNCIADO
Define un icono de "Home" (una casita) usando `<symbol>` con su propio `viewBox="0 0 20 20"`.
Dibuja el icono en el lienzo principal dos veces:
1. Pequeño (20x20).
2. Gigante (100x100).
Observa cómo el grosor de línea se escala o se mantiene según cómo lo definiste (si usaste `vector-effect` o no, aunque esto es extra). Lo importante es que funcione el redimensionado mediante atributos `width/height` en el `<use>`.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 200">
  <defs>
    <symbol id="icon-home" viewBox="0 0 20 20">
      <path d="M10 2 L2 10 H5 V18 H15 V10 H18 Z" />
    </symbol>
  </defs>
  
  <use href="#icon-home" x="10" y="10" width="20" height="20" />
  <use href="#icon-home" x="50" y="50" width="100" height="100" />
</svg>
```
