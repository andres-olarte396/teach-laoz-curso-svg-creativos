# EVALUACIÓN: GRUPOS Y TRANSFORMACIONES

## CUESTIONARIO

### Pregunta 1: Herencia de Estilos

Tienes un `<g fill="red">` que contiene un `<circle>` y un `<rect fill="blue">`. ¿De qué color será el círculo y de qué color el rectángulo?

- a) Ambos rojos.
- b) Círculo rojo, Rectángulo azul.
- c) Ambos azules.

### Pregunta 2: Origen de Rotación

Si aplicas `transform="rotate(45)"` a un cuadrado en el centro de la pantalla (100,100), ¿qué sucede?

- a) Rota 45 grados sobre su propio centro.
- b) Rota 45 grados orbitando alrededor de la esquina superior izquierda (0,0) del lienzo.
- c) No pasa nada si no especificas eje.

---

## SOLUCIONARIO

### Pregunta 1: Solución

**Respuesta**: b) Círculo rojo, Rectángulo azul.
**Razón**: La herencia en SVG es débil; los estilos explícitos en el hijo (`fill="blue"`) sobrescriben a los del padre. El círculo, al no tener estilo propio, hereda el rojo.

### Pregunta 2: Solución

**Respuesta**: b) Rota orbitando alrededor del (0,0).
**Razón**: El origen de transformación por defecto es siempre `(0,0)` del sistema de coordenadas actual, no el centro del objeto.
