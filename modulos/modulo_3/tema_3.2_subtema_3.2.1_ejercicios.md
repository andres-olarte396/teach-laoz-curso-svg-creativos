# BANCO DE EJERCICIOS: INTERACTIVIDAD BÁSICA

## METADATA
- **Módulo**: SVG Vivo - Animación e Interactividad
- **Tiempo total estimado**: 45 minutos
- **Nivel de ruta**: Intermedia

---

## EJERCICIO 1: Botones Musicales (CSS Hover)

### METADATA
- **Dificultad**: ⭐ Básico
- **Conceptos evaluados**: `:hover`, `:active`, `cursor`.

### ENUNCIADO
Dibuja 3 teclas de piano (rectángulos blancos).
Usa CSS para que:
1. Al pasar el mouse (`:hover`), la tecla se ponga gris claro.
2. Al hacer clic (`:active`), la tecla se ponga gris oscuro y se achique ligeramente (`transform: scale(0.98)`).
3. El cursor cambie a "pointer".

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 300 100">
  <style>
    .tecla {
      fill: white;
      stroke: black;
      transition: fill 0.2s, transform 0.1s;
      transform-origin: center;
      cursor: pointer;
    }
    .tecla:hover { fill: #eee; }
    .tecla:active { fill: #ccc; transform: scaleY(0.95); }
  </style>
  
  <rect class="tecla" x="10" y="10" width="80" height="80" />
  <rect class="tecla" x="100" y="10" width="80" height="80" />
  <rect class="tecla" x="190" y="10" width="80" height="80" />
</svg>
```

---

## EJERCICIO 2: El Interruptor de Luz (JS Toggle)

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: `onclick`, manipulación de atributos.

### ENUNCIADO
Dibuja una bombilla (círculo) y un interruptor (rectángulo).
Escribe un pequeño script (dentro del SVG o fuera) para que al hacer clic en el interruptor, la bombilla cambie de Negro (apagada) a Amarillo (encendida).
El interruptor también debería cambiar visualmente (ej. color verde si ON, rojo si OFF).

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 200 100">
  <circle id="foco" cx="50" cy="50" r="30" fill="black" />
  
  <rect id="switch" x="100" y="30" width="60" height="40" fill="darkred" rx="5" 
        style="cursor: pointer" />
  <text x="130" y="55" fill="white" text-anchor="middle" pointer-events="none">ON/OFF</text>
  
  <script>
    const foco = document.getElementById('foco');
    const btn = document.getElementById('switch');
    let encendido = false;
    
    btn.addEventListener('click', () => {
      encendido = !encendido;
      if (encendido) {
        foco.setAttribute('fill', 'yellow');
        btn.setAttribute('fill', 'green');
      } else {
        foco.setAttribute('fill', 'black');
        btn.setAttribute('fill', 'darkred');
      }
    });
  </script>
</svg>
```

---

## EJERCICIO 3: Hitbox Invisible (Usabilidad)

### METADATA
- **Dificultad**: ⭐⭐ Intermedio
- **Conceptos evaluados**: Áreas de clic aumentadas.

### ENUNCIADO
Tienes un icono de "Cerrar" (X) hecho con dos líneas muy finas (`stroke-width: 1`).
Es muy difícil hacerle clic.
Mejora la usabilidad añadiendo un círculo transparente debajo (o encima) de la X que sirva como área de clic (hitbox) grande (ej. radio 20px).
El efecto `:hover` debe activarse cuando tocas el área invisible, no solo la línea fina.
Pista: Agrupa líneas y círculo invisible en un `<g class="boton">`.

### SOLUCIÓN MODELO
```xml
<svg viewBox="0 0 100 100">
  <style>
    .btn-cerrar { cursor: pointer; }
    /* Al pasar sobre el grupo, pintamos las líneas hijas */
    .btn-cerrar:hover line { stroke: red; }
  </style>

  <g class="btn-cerrar">
    <!-- Hitbox invisible pero clickable -->
    <circle cx="50" cy="50" r="25" fill="transparent" />
    
    <!-- Icono visual -->
    <line x1="40" y1="40" x2="60" y2="60" stroke="black" stroke-width="2" />
    <line x1="60" y1="40" x2="40" y2="60" stroke="black" stroke-width="2" />
  </g>
</svg>
```
