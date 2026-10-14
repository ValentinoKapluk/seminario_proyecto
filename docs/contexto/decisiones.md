# Registro de Decisiones de Arquitectura (ADRs) — Epic Sneakers

## ADR-001: Adopción de TailwindCSS vía CDN
- **Contexto:** El proyecto busca combinar velocidad de maquetación profesional y diseño responsivo moderno con fines pedagógicos sin requerir instalación pesada de Node/npm en el cliente final.
- **Decisión:** Se utiliza TailwindCSS CDN (`<script src="https://cdn.tailwindcss.com"></script>`) configurado con clases de modo oscuro (`darkMode: 'class'`) y temas de color personalizados.
- **Consecuencias:** Desarrollo ágil, clases de utilidad declarativas, cero necesidad de compilar CSS externo.

## ADR-002: Modo Oscuro por Defecto con Persistencia Local
- **Contexto:** El usuario solicitó modo oscuro como tema base, pero con la posibilidad de alternar a modo claro a voluntad.
- **Decisión:** Implementar selector de tema que aplique o retire la clase `dark` en el elemento `<html>`, guardando la preferencia del usuario en `localStorage`.
- **Consecuencias:** Experiencia de usuario consistente entre recargas de página y cumplimiento del requisito de diseño.

## ADR-003: Estructura Monolítica Autónoma en un Único Archivo `index.html`
- **Contexto:** Se busca un código limpio, educativo y de fácil distribución que no requiera backend ni configuraciones de servidor complejas.
- **Decisión:** Todo el marcado HTML5, las directivas Tailwind y el script de interactividad residen en `index.html` de manera modular y ordenada mediante comentarios de sección.
- **Consecuencias:** Facilidad de revisión para docentes y estudiantes, portabilidad inmediata.

## ADR-004: Sistema de Modales y Feedback Visual del Formulario
- **Contexto:** Las tarjetas deben ofrecer detalles adicionales sin recargar ni navegar a otra página, y el formulario debe orientar al usuario con avisos claros.
- **Decisión:** Modales manipulados por el DOM con transiciones accesibles, y banner de alerta condicional (mensaje de error si faltan campos; mensaje *"Los datos han sido enviados correctamente"* al completarlo).
- **Consecuencias:** UX dinámica, reactiva y clara sin librerías externas pesadas.
