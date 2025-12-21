## RECURSOS VISUALES: PROYECTO FINAL

### 1. Arquitectura del Widget SVG

**Concepto**: Estructura de capas de una aplicación SVG interactiva.
**Tipo**: Mermaid

```mermaid
graph TD
    subgraph SVG_File [Archivo SVG: weather-mars.svg]
        direction TB
        
        DEFS[<defs>\nBiblioteca Invisible]
        STYLE[<style>\nAnimaciones CSS]
        SCRIPT[<script>\nLógica JS]
        
        subgraph BODY [Cuerpo Visible]
            BG[Fondo\n(Rect + Gradient)]
            CONTENT[Contenido\n(Textos + Use Icon)]
            UI[Interfaz\n(Botón Scan)]
        end
    end
    
    DEFS -.->|Referencia (xlink:href)| CONTENT
    DEFS -.->|Relleno (fill:url)| BG
    STYLE -->|Afecta a| BODY
    SCRIPT -->|Escucha Eventos| UI
    SCRIPT -->|Modifica| CONTENT
    
    style DEFS fill:#f9f,stroke:#333,stroke-width:2px
    style BODY fill:#e1f5fe,stroke:#01579b
    style SCRIPT fill:#fff3e0,stroke:#e65100
```
