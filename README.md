# FranciscoJManasAlvarez.github.io

Web personal de Francisco José Mañas Álvarez (Departamento de Informática y Automática, ETSI
Informática, UNED), publicada con GitHub Pages en <https://franciscojmanasalvarez.github.io/>.

## Estructura

```
index.html            Portada
sobre-mi.html          Bio, líneas de trabajo y enlaces
contacto.html          Datos de contacto
cursos/
  index.html            Listado de los tres cursos del programa de Formación Permanente en ROS 2
  iniciacion.html        Página del curso "Introducción a la Robótica con ROS 2" (2025/26)
assets/
  style.css             Hoja de estilos compartida por todas las páginas
  img/                   Imágenes (foto personal, etc.)
```

HTML/CSS plano, sin generador ni build: GitHub Pages sirve el repositorio tal cual desde la rama
`main`. Para previsualizar en local basta con abrir `index.html` en un navegador (o servir la
carpeta con `python3 -m http.server`).

## Cómo ampliar el sitio

- **Nueva página de curso**: copia `cursos/iniciacion.html` como plantilla, ajusta el temario y el
  enlace al repositorio de GitHub del curso correspondiente, y añade la tarjeta en `cursos/index.html`
  (quitando el badge "Próximamente").
- **Nueva sección en el menú**: añade el `<a>` correspondiente en el bloque `<nav class="site-nav">`
  de *todas* las páginas (cabecera repetida en cada archivo, no hay layout compartido).
- **Estilos**: todo el diseño vive en `assets/style.css`, con variables CSS en `:root` (colores,
  radios, sombras) y un bloque `@media (prefers-color-scheme: dark)` para modo oscuro automático.
- **Sobre mí / Contacto**: contenido editable directamente en `sobre-mi.html` y `contacto.html`
  (bio, líneas de trabajo como `<li>` en `.tag-list`, enlaces en `.link-list`).

## Publicación

GitHub Pages está configurado para servir desde `main` / raíz. Cualquier cambio empujado a `main`
se publica automáticamente en unos minutos.

## Licencia

Contenido y código de esta web: © Francisco José Mañas Álvarez.
