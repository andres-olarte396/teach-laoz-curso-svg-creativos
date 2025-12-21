# GUIÓN: IMPLEMENTACIÓN Y REFINAMIENTO

## FICHA TÉCNICA
- **Duración**: 6-7 minutos
- **Tono**: Profesional y conclusivo.

---

### 00:00 - INTRODUCCIÓN

**[LOCUTOR]**:
Ha llegado el momento de la verdad.
Tenemos el plano. Tenemos las herramientas.
Ahora, vamos a escribir el código final de nuestro Widget de Clima Marciano.
Abre tu editor de texto. Crea un archivo `weather-mars.svg`. Empezamos.

---

### 00:45 - EL ESQUELETO (ESTRUCTURA)

**[LOCUTOR]**:
Lo primero: La etiqueta `<svg>`. Le daremos un `viewBox` cómodo, digamos `0 0 400 300`.
Inmediatamente abrimos `<defs>`. Aquí definiremos nuestro gradiente de atmósfera roja y nuestro icono de Sol.
Recuerda: Si está en `defs`, no se ve. Es solo potencial.

---

### 01:30 - EL CUERPO (CONTENIDO)

**[LOCUTOR]**:
Ahora pintamos el fondo: `<rect width="100%" height="100%" fill="url(#atmósfera)" />`.
Y usamos un grupo `<g>` para contener todos nuestros textos e iconos.
¿Por qué un grupo? Porque si luego queremos mover todo el widget 50 píxeles a la derecha, solo movemos el grupo. Inteligente, ¿verdad?

---

### 02:15 - LA VIDA (ANIMACIÓN Y JS)

**[LOCUTOR]**:
Se ve bien, pero está muerto.
Vamos a añadir CSS. Una animación `@keyframes spin` para que el sol gire lentamente.
Y finalmente, un poco de JavaScript.
`document.getElementById`... `addEventListener`.
Hacemos que al pulsar el botón "SCAN", la temperatura cambie aleatoriamente.
Ahora sí. Ahora "se siente" real.

---

### 03:00 - POLISHING (PULIDO)

**[LOCUTOR]**:
Un novato pararía aquí. Un profesional pule los detalles.
¿El cursor cambia a manita sobre el botón? Añade `cursor: pointer`.
¿El texto es legible? Ajusta el contraste.
¿Es accesible? Añade una etiqueta `<title>`.

---

### 03:45 - CIERRE DEL CURSO

**[LOCUTOR]**:
¡Lo has conseguido!
Has empezado dibujando rectángulos y has terminado construyendo una aplicación interactiva vectorial completa.
Ahora tienes un superpoder: Puedes crear gráficos que cargan instantáneamente, se ven nítidos en cualquier pantalla y responden al usuario.
El mundo del SVG es tuyo. ¡Ve y crea algo asombroso!
