# miweb — Portfolio de Alex de las Morenas

Portfolio personal de una página para buscar prácticas o un primer empleo como desarrollador web en Córdoba y Granada. Es HTML, CSS y JavaScript estáticos: se abre directamente, sin build ni dependencias.

## Stack

- Lenguaje: HTML5, CSS3 y JavaScript vanilla (una IIFE, sin módulos).
- Framework / runtime: ninguno; se sirve como archivos estáticos. Python solo para el servidor local.
- Base de datos: ninguna.
- Tests: ninguno. Tampoco hay lint, typecheck ni build.

## Comandos

- `python -m http.server 8000` — arranca el servidor en local (o abre `index.html` con doble clic).
- `node --check script.js` — única comprobación de sintaxis disponible.
- Comprobación visual:
  `& "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless=new --window-size=1440,5200 --screenshot=out.png file:///C:/Users/Alex/Desktop/miweb/index.html`
  Usa 1440/768/500 px y prueba el menú móvil abierto/cerrado, `prefers-reduced-motion` y sin JS.
- No inventes comandos `npm`/`pnpm`: no hay `package.json`.

## Estructura del proyecto

- `index.html` — todo el contenido de la web: inicio, sobre mí, habilidades, proyectos, experiencia y contacto.
- `styles.css` — sistema visual completo; tokens de diseño en `:root` y responsive.
- `script.js` — menú móvil, observer de revelado, enlace activo del menú y año del footer.
- `cv.pdf` — CV listo para descargar. Es un binario sin fuente editable en el repo.
- `favicon.svg` — icono de la pestaña (monograma AM).
- `README.md` — puesta en marcha, contenido pendiente, actualización del CV y despliegue.

## Convenciones

- Todo el texto va en español (`lang="es"`), con tono directo y sin inflar.
- Usa los tokens de `:root` (`--paper`, `--ink`, `--accent`, `--ease`…) en vez de valores a mano.
- `script.js` es una única IIFE: sin módulos, imports ni dependencias.
- Toda animación nueva necesita tres estados: normal, `prefers-reduced-motion` y sin JS/fallback visible.
- La clase `.js` la añade un script inline en `<head>`; si `script.js` falla, un timeout de 2,5 s añade `.reveal-fallback`.
- El revelado es `.reveal` + IntersectionObserver que añade `.is-visible`; el dibujo de diagramas se dispara con `.project.is-visible`.
- Las formas SVG animadas necesitan `pathLength="1"` en cada `rect`/`line`; sin eso el trazo se dibuja sólido en silencio. Los `line` con `marker-end` solo hacen fade.
- El menú móvil anima `visibility`/`opacity`/`pointer-events` mediante `.open`, no `display`.
- `.nav-cta` necesita `!important` porque la regla genérica `.site-nav a` también lo afecta.
- Breakpoints: 1000 px (rejilla de proyectos a una columna, se resetea el `order`), 860 px (menú móvil), 680 px (layout apilado).
- El CV (`cv.pdf`) repite el contacto y la experiencia de `index.html`: si cambian, actualiza el PDF fuera del repo.

## No hagas

- No añadas build, frameworks, gestor de paquetes ni dependencias.
- No inventes experiencia, fechas ni datos de contacto. LinkedIn es el único perfil real; email y GitHub están pendientes (TODO en la sección de contacto).
- No vuelvas a `display:none` para el menú móvil: rompe la transición y el foco.
- No conviertas las tarjetas de proyecto en enlaces ni añadas hover que sugiera que se pueden clicar.
- No añadas `canonical` ni `og:image` hasta que exista la URL de despliegue.
- No intentes regenerar `cv.pdf` desde el repo: no hay fuente editable.
- No cambies el breakpoint de la cabecera sin confirmarlo con el dueño (ver «Problema conocido»).

## Flujo de trabajo

- Antes de una tarea no trivial, propón un plan y espera mi OK.
- Una tarea a la vez; al terminar, dime qué cambiaste para que lo revise.
- Si no estás seguro al 80%, pregunta. No inventes.

## Documentación

- `README.md` — setup local, contenido pendiente, actualización del CV y publicación (GitHub Pages / Netlify).

## Problema conocido

- Entre 861 y 1000 px la marca y la navegación de la cabecera se parten en dos líneas. Es previo a los últimos cambios; confírmalo con el dueño antes de tocarlo.
