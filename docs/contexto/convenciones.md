# Convenciones de Diseño y Código — Epic Sneakers

## 1. Tipografía y Textos
- **Familia Tipográfica:** Google Fonts [`Roboto`](https://fonts.google.com/specimen/Roboto) (pesos 400, 500, 700 y 900).
- **Títulos:** En negrita (`font-bold` / `font-black`), con espaciado controlado (`tracking-tight`).
- **Cuerpo y Párrafos:** Peso regular (`font-normal`), tamaño legible (14px a 16px) y alto contraste con el fondo.
- **Textos Alternativos:** Toda etiqueta `<img>` debe contar con un atributo `alt` descriptivo.

## 2. Paleta Cromática y Modos de Visualización

| Elemento | Modo Oscuro (Por Defecto) | Modo Claro (Alternativo) |
| :--- | :--- | :--- |
| **Fondo Principal** | Azul noche profundo (`#0b1329` / Tailwind: `bg-slate-950` / `bg-[#0b1329]`) | Blanco puro (`#ffffff` / Tailwind: `bg-white`) |
| **Fondo de Tarjetas** | Azul pizarra oscuro (`bg-slate-900/80` con bordes sutiles `border-slate-800`) | Blanco grisáceo suave (`bg-slate-50` con bordes `border-slate-200`) |
| **Color de Texto** | Blanco (`text-white`) y gris claro (`text-slate-300`) | Negro carbón (`text-slate-900`) y gris oscuro (`text-slate-600`) |
| **Gradiente Primario** | Gradiente Cian: `from-cyan-400 to-blue-500` | Gradiente Cian: `from-cyan-500 to-blue-600` |
| **Gradiente Secundario** | Gradiente Rojo: `from-rose-500 to-red-600` | Gradiente Rojo: `from-rose-600 to-red-600` |

## 3. Comportamientos y Micro-interacciones
- **Cursor:** Todo botón, enlace, tarjeta cliqueable o selector debe forzar `cursor-pointer`.
- **Transiciones:** Utilizar `transition-all duration-300 ease-in-out` para suavizar cambios de tonalidad, elevación o sombras.
- **Hover en Tarjetas:** Elevación leve (`-translate-y-1.5`), sombra acentuada (`shadow-xl shadow-cyan-500/10`) y zoom sutil en imágenes (`scale-105`).
- **Hover en Botones:** Aumento sutil de luminosidad o desplazamiento de gradiente.

## 4. Estándares de Código HTML y JS
- **HTML5 Semántico:** Uso riguroso de `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<button>`, `<footer>`.
- **No Inline Styles:** Cero atributos `style="..."`; todos los estilos gestionados mediante clases de TailwindCSS.
- **JavaScript Limpio:** Funciones modulares, nombres descriptivos en español/inglés coherente, manejo estricto de eventos (`addEventListener`) y comentarios pedagógicos.
