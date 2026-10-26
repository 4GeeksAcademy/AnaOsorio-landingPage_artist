# Plan técnico aprobado: landing page del artista

## Estado y alcance

Plan actualizado por indicación del usuario: contenido editable directamente en
HTML, sin archivos JSON de datos, generador ni dependencias. La demostración
presenta a Alma Valcárcel, artista escénica y narradora ficticia. El usuario
autoriza inventar identidad, biografía, proyectos, retrato, eventos y correos,
siempre identificados como ficción y sin atribuciones a una persona real.
JSON-LD de tipo `Person` se mantiene como excepción autorizada para SEO, no como
fuente de datos de los eventos.

Se mantienen los requisitos y criterios de aceptación de
[spec.md](../001-landing-artist/spec.md) y las reglas de
[AGENTS.md](../../AGENTS.md).

## Archivos previstos

- `index.html`: página estática para publicación con estructura semántica,
   navegación, contenido, metadatos y datos estructurados del personaje ficticio.
- `styles.css`: estilos separados, Flexbox, foco visible y reglas responsivas.
- `assets/images/retrato-artista-ficticio.webp`: ilustración bitmap original,
  creada con dibujo programático temporal y optimizada a WebP: 640 × 800 píxeles,
  12 232 bytes y sin EXIF. No es una fotografía ni representa a una persona real.
- El borrador inicial de `templates/` ya se trasladó a `index.html` y se retiró.
   Las siguientes modificaciones se harán directamente en la página raíz para
   evitar duplicados; la demostración no requiere datos de una persona real.

## Contenido y datos de ejemplo

El contenido se editará directamente en HTML:

- Artista ficticia: nombre, disciplina, presentación, biografía, retrato ilustrado y texto alternativo.
- Proyectos: título, descripción y enlace opcional.
- Eventos: dos o tres elementos con nombre, fecha, lugar y enlace opcional.
- Contacto: `hola@example.com` y `proyectos@example.com`, reservados para ejemplos,
  no operativos y sin canales oficiales reales.
- SEO: título y descripción de la página.
- Estado de demostración: aviso visible junto a los eventos ficticios y
   directiva de no indexación mientras queden ejemplos.

Los tres eventos tendrán nombres, fechas y lugares inventados y claramente
identificados como ficticios, sin usar contactos ni enlaces de terceros.
La biografía y los proyectos son inventados y están identificados como tales.
El retrato es una ilustración original con pie visible de ficción y alternativa
textual descriptiva. Se comprobó su decodificación y presupuesto de hasta 150 KiB
al crearlo, antes de que el visor de Copilot denegara acceso al recurso; no se
ha completado la revisión visual. El dibujo se exportó con herramientas temporales
fuera del proyecto, no con un generador que deba ejecutar la web.
La imagen tiene dimensiones declaradas y CSS responsivo. La demo conserva
`noindex` y los avisos de ficción; no se inventan permisos de fotografías ajenas.

## Edición y publicación sin JavaScript ejecutable

La web no consumirá archivos JSON ni ejecutará scripts de generación. Las
actualizaciones se harán en el HTML y no requerirán regeneración. El archivo
de datos creado con el enfoque anterior queda obsoleto y no será consumido.
No se accede ni se modifica el archivo excluido de Copilot.

El navegador recibirá HTML estático y CSS. La excepción para JSON-LD ya fue
autorizada y reflejada en AGENTS.md. Describe al personaje ficticio con `Person`,
nombre, ocupación, correo de ejemplo y descripción explícita de ficción,
coherentes con el contenido visible; no afirma que exista una persona real.

## Pasos principales

1. Preparar identidad, biografía, dos proyectos, tres eventos ficticios y correos
   reservados directamente en el HTML, con avisos claros de demostración.
   Crear y optimizar un retrato ilustrado original, sin fotografías de terceros.
2. Construir la plantilla semántica en español: header con navegación a Sobre mí,
   Trayectoria y Próximas presentaciones; main con IDs exactos `Hero`, `about`,
   `experience` y `events`; footer con correo. Incluir un único `h1`, jerarquía
   lógica y enlace para saltar al contenido principal.
3. Incorporar proyectos ficticios y tres tarjetas de eventos de ejemplo
   sin enlaces ni contactos de terceros, con aviso visible de demostración.
4. Aplicar CSS móvil primero con Flexbox. Dar a las secciones una altura mínima
   aproximada de un viewport, permitiendo crecer sin recortes. Incorporar foco
   visible, contraste suficiente y adaptación a distintos tamaños de pantalla.
5. Completar título, descripción y contenido coherente para SEO/GEO. Incorporar
   Schema.org `Person` para el personaje ficticio, bajo la excepción autorizada,
   declarando expresamente su naturaleza inventada.
6. Verificar los criterios de aceptación de la demostración; conservar los
   avisos y la no indexación sin exigir datos de una persona real.

## Verificación prevista

Estado actual: HTML validado con `html-validate`, referencias internas y
encabezados comprobados; contraste calculado con un mínimo de 6.13:1 para las
combinaciones de texto y fondo utilizadas. Tras instalar las bibliotecas del
sistema, Chromium completó el 26 de octubre de 2026 las comprobaciones de
legibilidad, teclado, tamaños de 320, 768 y 1440 píxeles y aceptación final.
La ampliación se verificó con CSS `zoom` al 200 % y reflujo equivalente con
ancho reducido a la mitad; no se utilizó el control manual de zoom del navegador.
Se corrigió la compresión de la biografía permitiendo ajuste de filas y se
repitieron con éxito las comprobaciones de zoom y tamaños normales.

La revisión visual del retrato fue retirada del alcance por el usuario. Las
pruebas utilizaron un sustituto neutro de sus mismas proporciones mediante
intercepción de peticiones, sin acceder al archivo excluido ni comprobar la
carga de ese WebP original. Se revisaron capturas de móvil y escritorio con
ese sustituto. Las tareas vigentes están completas; la evidencia de los
16 criterios y los límites de la comprobación figuran en [task.md](task.md).

- Comprobar que los eventos están en HTML y no dependen de archivos JSON ni scripts.
- Revisar estructura HTML, IDs únicos, navegación, correo y enlaces de eventos.
- Retrato: formato, dimensiones, peso y decodificación comprobados al generarlo;
   atributos, espacio responsivo y aviso ficticio revisados. Su contenido visual
   y la carga del archivo original están excluidos de la verificación final.
- Comprobar teclado, salto al contenido, foco, textos alternativos y contraste AA.
- Revisar anchos de 320, 768 y 1440 píxeles y zoom al 200 %, sin desbordamientos,
  solapamientos ni contenido recortado.
- Validar JSON-LD y su coherencia con la información visible y declarada ficticia.
- Confirmar ausencia de frameworks, dependencias, estilos en línea y JavaScript
  ejecutable; no publicar ejemplos como biografía, proyectos o eventos reales.

## Fuera de alcance

CMS, panel de administración, archivos JSON como fuente de contenido,
generadores, formularios con backend y cambios funcionales al servidor existente.