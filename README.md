# FranciscoJManasAlvarez.github.io

Web personal de Francisco José Mañas Álvarez (Departamento de Informática y Automática, ETSI
Informática, UNED), publicada con GitHub Pages en <https://franciscojmanasalvarez.github.io/>.

## Estructura

```
index.html              Portada
sobre-mi.html            Bio, líneas de trabajo, formación académica, experiencia laboral y enlaces
investigacion.html       Proyectos de I+D+i y divulgación científica (enlaza a Robotic Park Lab)
publicaciones.html       Revistas, congresos y capítulos de libro, con hueco de imagen por entrada
docencia.html            Formación Permanente, asignaturas, PFG/PFM dirigidos y tutorías UNED
contacto.html            Datos de contacto
cursos/
  iniciacion.html          Página del curso "Introducción a la Robótica con ROS 2" (2025/26)
  intermedio.html          Página del curso "ROS 2 intermedio" (2026/27)
  avanzado.html            Página del curso "Robótica avanzada con ROS 2" (2027/28)
assets/
  style.css               Hoja de estilos compartida por todas las páginas
  img/                     Imágenes (foto personal, etc.)
  img/publications/        Portadas / graphical abstracts de publicaciones (ver publicaciones.html)
  img/divulgacion/         Imágenes de eventos de divulgación (ver investigacion.html)
```

HTML/CSS plano, sin generador ni build: GitHub Pages sirve el repositorio tal cual desde la rama
`main`. Para previsualizar en local basta con abrir `index.html` en un navegador (o servir la
carpeta con `python3 -m http.server`).

## Cómo ampliar el sitio

- **Añadir una imagen a una publicación**: guarda el fichero en `assets/img/publications/` y
  sustituye, en `publicaciones.html`, el `<div class="pub-thumb">Añade portada</div>` de esa
  entrada por `<div class="pub-thumb"><img src="assets/img/publications/nombre.jpg" alt="..."></div>`.
- **Nueva publicación**: copia un bloque `<div class="card pub-card">…</div>` de
  `publicaciones.html` en la sección correspondiente (Revistas / Congresos nacionales / Congresos
  internacionales / Capítulos de libro).
- **Nueva asignatura, tutoría o TFG/TFM dirigido**: añade una tarjeta `.item-card` (asignaturas),
  una fila a la tabla `.temario` (tutorías), o un `<li>` a la lista de trabajos dirigidos, en
  `docencia.html`.
- **Propuestas de TFG/TFM**: sustituye la nota "en preparación" de la sección `#pfg-pfm` de
  `docencia.html` por las propuestas reales.
- **Nueva página de curso**: copia `cursos/iniciacion.html` como plantilla y añade la tarjeta
  correspondiente en la sección `#formacion-permanente` de `docencia.html`.
- **Nueva sección en el menú**: añade el `<a>` correspondiente en el bloque `<nav class="site-nav">`
  de *todas* las páginas (cabecera repetida en cada archivo, no hay layout compartido).
- **Estilos**: todo el diseño vive en `assets/style.css`, con variables CSS en `:root` (colores,
  radios, sombras) y un bloque `@media (prefers-color-scheme: dark)` para modo oscuro automático.
  Los patrones `.entry`, `.toc`, `.pub-card` e `.item-card` son reutilizables en cualquier página.

## Publicación

GitHub Pages está configurado para servir desde `main` / raíz. Cualquier cambio empujado a `main`
se publica automáticamente en unos minutos.

## Licencia

Contenido y código de esta web: © Francisco José Mañas Álvarez.
