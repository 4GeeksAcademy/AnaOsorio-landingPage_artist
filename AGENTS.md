# Instrucciones para la landing page del artista

## Alcance y tecnología

- Este proyecto es una landing page estática para un artista.
- No implementes cambios funcionales si la solicitud solo pide documentación, planificación o revisión.
- Usa únicamente HTML y CSS nativos. No agregues frameworks, bibliotecas, dependencias ni JavaScript.
- Excepción autorizada: se permite un bloque `<script type="application/ld+json">` para datos estructurados Schema.org válidos y respaldados por el contenido visible. No se permite JavaScript ejecutable.
- Mantén los estilos en un archivo CSS separado y enlázalo desde el HTML; no uses estilos en línea ni bloques `<style>`.

## HTML y CSS

- Escribe HTML semántico: usa los elementos según su propósito y estructura la página con regiones como `header`, `nav`, `main` y `footer` cuando correspondan.
- Mantén una jerarquía lógica de encabezados, comenzando con un único `h1` descriptivo.
- Usa Flexbox para los diseños y la distribución de contenido; evita depender de tablas para maquetar.
- Diseña de forma responsiva, priorizando pantallas pequeñas y adaptando el contenido con reglas CSS y media queries.
- Conserva una presentación legible y usable con distintos tamaños de pantalla y niveles de zoom.

## Accesibilidad

- Incluye el idioma correcto del contenido en el atributo `lang` de `html`.
- Asegura que los controles y enlaces puedan usarse con teclado y tengan un foco visible.
- Usa texto de enlace descriptivo, etiquetas asociadas a los campos de formulario y texto alternativo útil para imágenes informativas.
- No comuniques información únicamente mediante color y verifica que haya contraste suficiente entre texto y fondo.
- Evita elementos interactivos sin nombre accesible y conserva el propósito semántico de los elementos HTML.

## SEO y GEO

- Define un título de página único y una descripción concisa y fiel al contenido.
- Esta demostración puede incluir identidad, biografía, proyectos, eventos y retrato ilustrado inventados por autorización del usuario. Identifica claramente su carácter ficticio y no los atribuyas a una persona real.
- Usa únicamente correos reservados bajo `example.com` para los contactos ficticios; no inventes contactos de terceros ni presentes los ejemplos como canales operativos.
- Mantén el contenido claro y coherente, sin texto repetitivo para buscadores. Los datos de producción sobre una persona real sí requieren verificación y permisos de imagen.
- Usa encabezados descriptivos, enlaces comprensibles y nombres de archivo relevantes para los recursos.
- Proporciona texto alternativo que describa la información relevante de cada imagen; usa texto alternativo vacío para imágenes decorativas.
- Añade metadatos sociales o datos estructurados solo cuando sean pertinentes, válidos y respaldados por el contenido visible. Schema.org `Person` puede describir al personaje ficticio si su descripción declara expresamente que no representa a una persona real; conserva `noindex` en la demostración.
- Mantén la información del artista coherente en la página y no ocultes contenido importante a los motores de búsqueda.