# Especificación: landing page para un artista

## Objetivo y alcance

Definir una landing page de demostración en español para Alma Valcárcel,
artista escénica y narradora ficticia, con biografía, proyectos, agenda y contacto
inventados por autorización expresa del usuario. La implementación está autorizada.

## Requisitos

### Estructura y contenido

- Header con navegación a Sobre mí, Trayectoria y Próximas presentaciones.
- Sección con ID exacto `Hero`: bienvenida, nombre y presentación del artista.
- Sección con ID exacto `about`: biografía inventada y retrato ilustrado original,
  identificado como ficticio y sin atribuirlo a una persona real.
- Sección con ID exacto `experience`: proyectos realizados y su descripción.
- Sección con ID exacto `events`: entre dos y tres tarjetas de próximas
  presentaciones, con nombre, fecha, lugar y enlace descriptivo cuando exista
  una URL confirmada.
- Footer con correo de contacto enlazado mediante `mailto:`.
- Contenido en español, claro y coherente con su carácter de ficción. Se permite
  inventar identidad, biografía, proyectos, retrato, eventos y correos; no se
  presentarán como datos de una persona real ni como convocatorias operativas.
- Los correos usarán el dominio reservado `example.com`, con aviso de que son
  ejemplos no operativos. No incluir contactos ni supuestos canales de terceros.

### Diseño y tecnología

- Usar únicamente HTML semántico y CSS nativo en un archivo separado.
- Usar Flexbox para la distribución; no usar tablas para maquetar.
- No incorporar frameworks, bibliotecas, dependencias ni JavaScript ejecutable.
- Editar el contenido directamente en HTML, sin archivos JSON de datos ni
  generadores. Esto no elimina la excepción independiente para JSON-LD de `Person`.
- Cada sección principal debe ocupar aproximadamente la altura del viewport,
  con altura mínima y posibilidad de crecer según su contenido.
- Priorizar pantallas pequeñas y adaptar el diseño a móvil, tableta y escritorio.

### Accesibilidad

- Declarar el idioma español y utilizar regiones semánticas adecuadas.
- Incluir un único `h1` descriptivo y una jerarquía lógica de encabezados.
- Permitir navegación por teclado con foco visible y enlaces descriptivos.
- Ofrecer un enlace para saltar al contenido principal.
- Incluir texto alternativo útil en imágenes informativas y vacío en decorativas.
- Cumplir contraste WCAG AA y no transmitir información solo mediante color.
- Conservar contenido legible y controles utilizables al ampliar el zoom.

### SEO, GEO y datos estructurados

- Definir título de página y metadescripción únicos y fieles al contenido.
- Presentar información clara y coherente sobre el personaje ficticio y sus
  proyectos, sin prometer posicionamiento ni atribuirle canales oficiales reales.
- Usar encabezados descriptivos, enlaces comprensibles y nombres de recursos
  relevantes, sin repetición artificial de palabras clave ni contenido oculto.
- Incluir datos estructurados Schema.org de tipo `Person` en JSON-LD, con
  propiedades respaldadas por el contenido visible y descripción explícita de
  que es un personaje ficticio y no representa a una persona real.
- JSON-LD requiere un bloque `script` de tipo `application/ld+json`, que contiene
  datos y no código ejecutable. Su uso ya está autorizado como excepción a la
  regla de no JavaScript de AGENTS.md. No se usará para presentar ficción como
  información verificada sobre una persona real. Conservar `noindex` en la demo.

## Criterios de aceptación

1. La página está en español y contiene header, las cuatro secciones principales
   y footer dentro de una estructura HTML semántica.
2. Los IDs `Hero`, `about`, `experience` y `events` existen una sola vez y respetan
   exactamente las mayúsculas indicadas.
3. Los tres enlaces del header apuntan respectivamente a `about`, `experience`
   y `events`; al activarlos, el encabezado de destino queda visible.
4. El hero presenta a Alma Valcárcel; Sobre mí incluye biografía y retrato ilustrado;
   Trayectoria describe proyectos realizados.
  El retrato incluye aviso visible de ficción y alternativa textual útil;
  no se requiere una fotografía real para completar esta demostración.
  El archivo es `assets/images/retrato-artista-ficticio.webp`,
  con objetivo de 640 × 800 píxeles y hasta 150 KiB, dimensiones declaradas,
  sin deformación y adaptado mediante CSS. Solo se marca la tarea de imagen
  como terminada después de comprobar que existe, se decodifica y cumple
  el presupuesto; mientras no esté disponible, permanece pendiente.
5. Próximas presentaciones muestra dos o tres tarjetas con nombre, fecha y lugar.
  En demostración contiene tres eventos ficticios en HTML, con aviso visible y
  sin enlaces ni contactos de terceros. Los futuros enlaces reales serán
  descriptivos y tendrán destinos confirmados.
6. El footer incluye `hola@example.com` y `proyectos@example.com` mediante
  enlaces `mailto:`, con aviso de que son ejemplos no operativos.
7. Cada sección principal ocupa aproximadamente un viewport cuando su contenido
   es breve y crece sin recortes ni superposiciones cuando necesita más espacio.
8. A anchos de 320, 768 y 1440 píxeles no hay desbordamiento horizontal,
   superposiciones ni texto o controles recortados.
9. Al ampliar el zoom al 200 %, todo el contenido y los controles permanecen
   visibles o alcanzables y utilizables.
10. Todos los enlaces son accesibles mediante teclado, tienen foco visible y
    nombre comprensible; el enlace de salto permite llegar al contenido principal.
11. Se declara `lang="es"`, existe un único `h1` y los encabezados mantienen una
    jerarquía lógica. Las imágenes tienen texto alternativo apropiado.
12. El contraste alcanza al menos 4.5:1 para texto normal y 3:1 para texto grande;
    la información no depende exclusivamente del color.
13. El título y la metadescripción identifican el carácter ficticio del portafolio.
  La identidad, biografía, proyectos y contactos son coherentes entre secciones.
14. Bajo la excepción autorizada, el JSON-LD es JSON válido, utiliza el contexto
    `https://schema.org` y el tipo `Person`, y coincide con el contenido visible.
15. Los estilos están en CSS separado y la distribución utiliza Flexbox.
    No hay frameworks, dependencias, estilos en línea ni JavaScript ejecutable.
16. La ficción está identificada visiblemente, se conserva la no indexación
  y no se presentan correos o eventos como canales o convocatorias reales.

## Demostración y producción

- La demostración no depende de obtener datos reales, fotografía o canales oficiales.
- Mantener avisos de ficción y no indexación mientras se utilice esta identidad.
- Convertirla en un sitio de una persona real sería un cambio posterior: requerirá
  datos verificados, permisos de imagen, contacto operativo y revisión de JSON-LD.