# RECURSO VISUAL: ILUSTRACIÓN DEL TEMA

![Ilustración Subtema 0.2](../../media/ilustraciones/ilustracion_subtema_0.2.svg)

# XML: LA GRAMÁTICA DEL SVG

**Tiempo estimado**: 15 minutos
**Nivel**: Fundamentos
**Prerrequisitos**: Ninguno

## ¿Por qué importa este concepto?
SVG no es magia oscura. Es texto. Específicamente, es **XML** (eXtensible Markup Language).
Si vienes de HTML, esto te parecerá familiar pero... ¡Cuidado! XML es el profesor estricto que te reprueba si olvidas una comilla.

---

## 1. La Sintaxis Estricta
En HTML, a veces puedes escribir `<br>` sin cerrar y el navegador te perdona. En XML, eso es un error fatal.
- **Regla 1**: Toda etiqueta abierta debe cerrarse. `<rect>` -> `<rect />` o `<rect>...</rect>`.
- **Regla 2**: Los atributos siempre van entre comillas. `width=100` ❌ -> `width="100"` ✅.
- **Regla 3**: Sensible a mayúsculas. `<ViewBox>` no es lo mismo que `<viewBox>`.

## 2. Estructura de Árbol
XML es jerárquico.
- Tienes una raíz (`<svg>`).
- Tienes hijos (`<circle>`, `<g>`, `<rect>`).
- Un hijo no puede cerrarse fuera de su padre.

```xml
<!-- Correcto -->
<g>
  <circle />
</g>

<!-- Incorrecto (Intersectado) -->
<g>
  <circle>
</g>
  </circle> 
```

---

## Conexión con conocimientos previos
Piensa en HTML como "inglés coloquial" (se entiende aunque gramaticalmente no sea perfecto).
XML es "código legal" o "matemáticas". Una coma fuera de lugar cambia el significado o invalida el documento.

---

## Resumen del concepto

**En una frase**: SVG es código de texto estricto que describe formas.

**Cuándo usarlo**: Siempre que escribas SVG a mano o lo depures.

**Siguiente paso**: Ahora que sabemos escribir las palabras, aprendamos dónde colocarlas: **El Sistema de Coordenadas**.


## 🕹️ LABORATORIO VIRTUAL

> [!TIP]
> **Experiencia Práctica**: Simulación Interactiva: Repara el XML
> 
> [Abrir Simulación](../../recursos/simulaciones/sim_0.2_xml_syntax.html)

