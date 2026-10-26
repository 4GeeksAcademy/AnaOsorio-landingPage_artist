# Tareas: landing page del artista

Basadas en [plan.md](plan.md) y [spec.md](spec.md).
Ejecución autorizada por el usuario, en orden y sin avanzar sobre tareas pendientes.

Cambio posterior autorizado: inventar identidad, biografía, proyectos, retrato,
eventos y correos para una demostración explícitamente ficticia. Contenido
directamente en HTML, sin archivos JSON de datos ni generador. No se requieren
datos reales para completar esta demo; no se utilizarán contactos de terceros.

## Estado de esta ejecución

- Demostración disponible en [index.html](../../index.html), con estilos externos
	y los cuatro destinos de navegación. El borrador de `templates/` fue retirado.
- Autorizado continuar con tareas independientes y dejar abiertas las bloqueadas.
- Implementados el diseño móvil primero, Flexbox, secciones de altura mínima
  aproximada al viewport, tarjetas, foco, biografía con retrato y proyectos.
- Validados HTML con `html-validate`, enlaces internos, IDs, encabezados,
	eventos y ausencia de JSON de datos o JavaScript ejecutable. JSON-LD de
	`Person` analizado y coherente con la ficción declarada. Contraste mínimo
	calculado entre las combinaciones de texto y fondo: 6.13:1.
- Verificación de navegador completada el 26 de octubre de 2026, después de
  instalar las bibliotecas del sistema: Chromium ejecutó las comprobaciones
  de legibilidad, teclado, tamaños, ampliación y aceptación final.
- Incorporados Alma Valcárcel, su biografía ficticia, dos proyectos inventados
	y dos correos reservados bajo `example.com`, identificados como no operativos.
- Creado un retrato ilustrado original de 640 × 800 píxeles, WebP de 12 232 bytes,
	sin EXIF; su decodificación se comprobó al generarlo. El visor de Copilot
  posteriormente lo excluyó. Su revisión visual fue retirada del alcance por
  indicación del usuario; no se considera una verificación realizada.

## Verificación final

- Todas las tareas vigentes completadas. Las tareas retiradas por el usuario
  no se cuentan como verificaciones realizadas.
- Chromium comprobó la página a 320, 768 y 1440 píxeles: texto legible, sin
  desbordamiento horizontal, secciones de al menos 90 % del viewport y sin
  solapamiento entre secciones, tarjetas y bloques de biografía.
- Recorrido real con Tab por los ocho enlaces, foco visible, salto al contenido
  activado con Enter y encabezados de destino visibles al activar las anclas.
- Ampliación al 200 % comprobada mediante CSS `zoom` y reflujo equivalente
  reduciendo a la mitad el ancho disponible, no mediante el control manual
  de zoom de Chromium. Texto y contactos siguen siendo alcanzables.
- La prueba detectó compresión de la biografía a 768 píxeles con ampliación.
  Se corrigió permitiendo ajuste de filas y una base de 18 rem para el texto;
  después pasaron nuevamente zoom y tamaños normales.
- Las pruebas interceptaron la petición del retrato antes de acceder al archivo
  y devolvieron un rectángulo neutro de 640 × 800. Se verificó su espacio y
  proporción, no el contenido ni la carga del WebP original excluido.
- Capturas de móvil y escritorio revisadas con ese sustituto. No se eludió
  la exclusión ni se reintrodujo la revisión del retrato retirada del alcance.
- Herramientas y capturas temporales fuera del proyecto; no se añadieron
  dependencias de ejecución ni scripts ejecutables a la web.

### Evidencia de aceptación

| Criterio | Comprobación |
| --- | --- |
| 1 | Idioma español y regiones header, nav, main y footer verificadas en DOM. |
| 2 | Cuatro IDs exactos y únicos. |
| 3 | Anclas activadas con teclado y encabezados visibles. |
| 4 | Identidad, biografía y dos proyectos presentes; atributos y espacio del retrato comprobados. Archivo verificado al generarlo; revisión visual retirada. |
| 5 | Tres eventos ficticios con títulos, fechas válidas, lugares y aviso visible. |
| 6 | Dos enlaces mailto bajo example.com y aviso de no operatividad. |
| 7 | Secciones medidas con altura mínima de 90 % del viewport y crecimiento por contenido. |
| 8 | Mediciones y capturas en los tres anchos requeridos. |
| 9 | Ampliación CSS al 200 % y reflujo equivalente sin desbordamientos. |
| 10 | Ocho enlaces recorridos con Tab, nombres y foco visible comprobados. |
| 11 | lang es, un único h1, jerarquía y texto alternativo verificados. |
| 12 | Contraste mínimo calculado de 6.13:1 entre las combinaciones utilizadas. |
| 13 | Metadatos y contenido coherentes con Alma y su condición ficticia. |
| 14 | JSON-LD analizado, tipo Person y descripción explícita de ficción. |
| 15 | CSS externo, Flexbox y solo script de datos JSON-LD, sin JavaScript ejecutable. |
| 16 | Avisos de ficción, contactos no operativos y noindex conservados. |

## Registro de datos disponibles

- Confirmado: landing en español con presentación, biografía, proyectos,
  dos o tres eventos y correo de contacto; contenido editable directamente en HTML.
- Personaje ficticio: Alma Valcárcel, artista escénica y narradora de Ciudad Imaginaria.
- Biografía inventada: teatro comunitario y piezas de narración, movimiento
  e improvisación; el texto identifica explícitamente su carácter ficticio.
- Proyectos ficticios: Cartas al aire (2024) y El mapa de los gestos (2025).
- Retrato: ilustración original en `assets/images/retrato-artista-ficticio.webp`,
  con texto alternativo descriptivo y pie visible que niega que sea una foto real.
- Demostración: tres eventos inventados en HTML, sin enlaces ni contactos de terceros.
- Correos de ejemplo: `hola@example.com` y `proyectos@example.com`; no operativos.
- Sin canales oficiales reales ni contactos de terceros.
- Título, descripción y JSON-LD coherentes con Alma y su carácter de personaje ficticio.
- La demo conserva `noindex`. Datos reales y permisos de fotografía solo serían
  necesarios para una futura conversión a un sitio de una persona real.

## Decisiones sustituidas

La definición de campos y la creación inicial del JSON fueron completadas bajo
el plan anterior, pero ya no forman parte de la solución. Su validación y el
generador quedan cancelados, no completados. El archivo excluido no se consume
ni se modifica. JSON-LD de `Person` conserva su autorización independiente para SEO.
También quedan sustituidas las reglas que exigían confirmar datos reales,
sustituir la ilustración por una fotografía y retirar los avisos de ficción:
no son requisitos de esta demostración autorizada. No se marcan como tareas realizadas.
También se retiraron, por solicitud explícita del usuario, la revisión visual
del retrato y la tarea de recursos visuales cuyo único pendiente era esa imagen.
Se conservan los requisitos de texto alternativo y adaptación responsiva del HTML/CSS.

## 1. Preparación y datos

- [x] Registrar los datos confirmados y los pendientes del artista.
- [x] Obtener aprobación explícita para JSON-LD y reflejar la excepción en [AGENTS.md](../../AGENTS.md) antes de incorporarlo.
- [x] Incluir tres eventos de ejemplo directamente en HTML con nombre, fecha y lugar, sin JSON ni enlaces o contactos de terceros; identificarlos como ficticios.
- [x] Validar los tres eventos HTML: nombres distintos, fechas válidas, lugares y aviso visible de demostración.
- [x] Crear un retrato ilustrado original y guardarlo como `assets/images/retrato-artista-ficticio.webp`, a 640 × 800 píxeles y menos de 150 KiB, sin metadatos personales.
- [x] Comprobar al generarlo que se decodifica, mide 640 × 800 y ocupa 12 232 bytes; registrar que es una ilustración ficticia, no una fotografía real.

## 2. Plantilla HTML

- [x] Crear la plantilla en español con header, nav, main y footer; posteriormente trasladada a `index.html`.
- [x] Declarar `lang="es"`, enlazar `styles.css` e incluir un único `h1` y encabezados jerárquicos.
- [x] Añadir un enlace para saltar al contenido principal.
- [x] Crear la navegación a `about`, `experience` y `events` con textos descriptivos.
- [x] Crear la sección `Hero` con bienvenida, nombre y presentación del personaje ficticio.
- [x] Crear la sección `about` con biografía inventada, retrato ilustrado con texto alternativo y pie visible de ficción.
- [x] Crear la sección `experience` con dos proyectos ficticios, fechas y descripciones.
- [x] Crear la sección `events` con tres artículos de eventos ficticios, encabezados y fechas semánticas, sin enlaces inventados.
- [x] Añadir al footer dos correos reservados mediante `mailto:`, con aviso de que no son operativos y sin canales oficiales reales.

## 3. Publicación estática sin generador

- [x] Mostrar el aviso de eventos ficticios y conservar la directiva de no indexación durante la demostración.
- [x] Trasladar la demostración a `index.html`, ajustar el enlace CSS a `styles.css` y retirar el borrador para mantener una sola fuente de contenido.
- [x] Completar en `index.html` identidad, biografía, proyectos, retrato y contacto ficticios, con avisos de demostración.
- [x] Comprobar que la página estática no depende de archivos JSON de datos, generadores ni JavaScript ejecutable y que su CSS existe.

## 4. Diseño y accesibilidad

- [x] Crear `styles.css` separado, con diseño móvil primero y distribución mediante Flexbox.
- [x] Dar a cada sección principal una altura mínima aproximada de un viewport y permitir que crezca con el contenido, sin alturas fijas.
- [x] Implementar las reglas de adaptación de navegación, retrato, proyectos y tarjetas a móvil, tableta y escritorio mediante media queries; la verificación visual queda en las tareas de tamaños y zoom.
- [x] Definir estilos de foco visible, enlace de salto y separación para los destinos de navegación.
- [x] Ajustar el contraste a WCAG AA y evitar información transmitida solo mediante color.
- [x] Asegurar textos legibles e imágenes responsivas sin desbordamientos; comprobado en Chromium a 320, 768 y 1440 píxeles con sustituto neutro del retrato excluido para medir su espacio sin revisarlo.

## 5. SEO, GEO y datos estructurados

- [x] Escribir título y metadescripción directamente en HTML, fieles al estado de demostración y sin atribuir hechos inventados.
- [x] Ajustar título y descripción al personaje de Alma Valcárcel, identificando la ficción.
- [x] Comprobar coherencia de nombre, biografía, proyectos y contactos reservados, sin canales oficiales inventados ni texto oculto para buscadores.
- [x] Incorporar JSON-LD válido con contexto `https://schema.org` y tipo `Person`, declarando que describe un personaje ficticio y no una persona real.
- [x] Comprobar que nombre, ocupación y correo del JSON-LD coinciden con el contenido visible y que su descripción identifica la ficción.

## 6. Verificación y publicación

- [x] Validar el HTML y comprobar que los IDs `Hero`, `about`, `experience` y `events` son únicos y exactos.
- [x] Recorrer la página con teclado y comprobar salto al contenido, foco visible y nombres accesibles en Chromium a 320, 768 y 1440 píxeles.
- [x] Revisar la jerarquía de encabezados y el texto alternativo descriptivo del retrato informativo; no hay imágenes decorativas.
- [x] Medir contraste: al menos 4.5:1 en texto normal y 3:1 en texto grande.
- [x] Revisar anchos de 320, 768 y 1440 píxeles sin solapamientos, recortes ni desplazamiento horizontal; mediciones en Chromium y capturas de móvil y escritorio revisadas con sustituto neutro del retrato.
- [x] Comprobar ampliación al 200 % mediante zoom CSS y reflujo equivalente con ancho reducido a la mitad: texto sin desbordamiento y contactos alcanzables en los tres tamaños; no se utilizó el control manual de zoom del navegador.
- [x] Validar JSON-LD y verificar ausencia de frameworks, dependencias de ejecución, estilos en línea y JavaScript ejecutable.
- [x] Conservar los avisos de ficción y `noindex`, incluyendo la condición no operativa de los correos; no exigir datos reales para la demo.
- [x] Comprobar los 16 criterios de aceptación de la demostración, según la evidencia y las exclusiones documentadas en la verificación final.