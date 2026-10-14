# Bitácora de Errores Comunes y Gotchas de Maquetado — Epic Sneakers

En este documento se registran los problemas frecuentes de desarrollo web para prevenirlos activamente durante la codificación.

| Gotcha / Error Típico | Causa Frecuente | Medida de Prevención y Solución en Código |
| :--- | :--- | :--- |
| **Scroll horizontal accidental en móviles** | Anchos fijos mayores a `100vw` o márgenes negativos sin contenedor acotado. | Aplicar `max-w-full` y `overflow-x-hidden` en el contenedor principal o `<body>`. |
| **Falta de accesibilidad en imágenes** | Omitir el atributo `alt` o dejarlo vacío. | Incluir siempre descripciones semánticas y claras en cada `alt="..."` de las zapatillas. |
| **Elementos cliqueables no semánticos** | Usar `<div>` o `<span>` con evento de clic en lugar de `<button>`. | Utilizar exclusivamente etiquetas `<button type="button">` con `cursor-pointer` y accesibilidad por teclado. |
| **Contraste de texto deficiente en modo oscuro o claro** | Olvidar definir colores de texto específicos para cada modo. | Usar clases explícitas `text-slate-900 dark:text-white` para garantizar legibilidad en ambos estados. |
| **Desfase en la validación del formulario** | No advertir al usuario qué campo específico falta completar antes de enviar. | Comprobar que los campos `nombre`, `email` y `mensaje` tengan valores no vacíos con `trim()` y desplegar advertencia visual en pantalla. |
| **Errores ortográficos en textos comerciales** | Copiar nombres o categorías sin revisión. | Revisar acentuación, puntuación y consistencia en el nombre "Epic Sneakers" y las descripciones. |
