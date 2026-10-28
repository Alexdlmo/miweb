# miweb — Portfolio de Alex de las Morenas

Portfolio personal de una página para buscar **prácticas o un primer empleo como desarrollador web** en Córdoba y Granada.

Hecho con **HTML, CSS y JavaScript**, sin frameworks ni proceso de build. Incluye diseño responsive, menú móvil, animaciones sutiles, accesibilidad y SEO básico.

## Archivos

| Archivo | Para qué sirve |
| --- | --- |
| `index.html` | Todo el contenido: inicio, sobre mí, habilidades, proyectos, experiencia y contacto |
| `styles.css` | Diseño, colores y responsive |
| `script.js` | Menú móvil, animaciones y enlace activo del menú |
| `favicon.svg` | Icono de la pestaña (monograma AM) |
| `cv.pdf` | CV listo para descargar desde la web |

## Ver la web en local

Abre `index.html` con doble clic. Para probarla como en un servidor real:

```bash
# Desde la carpeta miweb
python -m http.server 8000
```

Y abre `http://localhost:8000`.

## Contenido pendiente

La web ya usa el perfil real, pero faltan estos datos:

1. **Email profesional.** Ahora el contacto principal es LinkedIn. Cuando lo tengas, añádelo en `index.html`:
   - en el botón principal de la sección de contacto (`mailto:tu@email.com`),
   - en los enlaces de contacto,
   - y en `cv.pdf`, editándolo fuera del repo.
2. **GitHub.** No se ha incluido porque no se ha facilitado el perfil. Si lo tienes, añade el enlace en el hero y en contacto.
3. **Proyectos.** Los tres proyectos actuales son reales: este portfolio, el proyecto interno de SB Software y el conector con PrestaShop. Si tienes proyectos de clase o personales con demo o repositorio público, sustitúyelos o añádelos.
4. **Fechas de DAM y DAW.** Están tomadas de LinkedIn (`DAM: sept. 2024 — actualidad`, `DAW: sept. 2025 — may. 2026`). Revísalas antes de publicar.
5. **Idiomas.** Solo se indica español nativo. Añade tu nivel de inglés si quieres incluirlo.
6. **Foto.** La identidad es tipográfica, sin foto. Si quieres añadir una, colócala en el hero o en «Sobre mí» y ajusta el layout.

## Actualizar el CV

`cv.pdf` no tiene fuente editable en el repositorio. Para cambiarlo, edita el documento original fuera del repo (Word, Google Docs, Canva…) y sustituye `cv.pdf` en esta carpeta.

## Publicar gratis

### GitHub Pages
1. Crea un repositorio en GitHub y sube el contenido de `miweb`.
2. Ve a **Settings → Pages**.
3. En *Source* elige la rama `main` y la carpeta `/ (root)`.
4. Tu web estará en `https://tuusuario.github.io/nombre-del-repo/`.

### Netlify Drop
1. Entra en [app.netlify.com/drop](https://app.netlify.com/drop).
2. Arrastra la carpeta `miweb`.
3. Listo. Puedes conectar un dominio propio después.

## Antes de enviar candidaturas

- Revisa que el email y el CV estén actualizados.
- Prueba todos los enlaces (LinkedIn y descarga del CV).
- Comprueba la web en el móvil.
- Pasa Lighthouse en Chrome DevTools → Lighthouse.
- No inventes experiencia: es mejor un portfolio modesto y honesto.

## Ideas para más adelante

- Añadir email y GitHub.
- Publicar un proyecto personal con demo y código.
- Modo oscuro.
- Página de detalle para cada proyecto.
- Versión en inglés.
- Imagen Open Graph para compartir en LinkedIn.
