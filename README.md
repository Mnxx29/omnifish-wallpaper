# Generador de fondos Omnifish

Formulario para crear fondos de pantalla de los equipos de soporte de cada centro de cultivo. Conserva el fondo y logo de la plantilla Omnifish y genera el texto a la resolución seleccionada.

**Sitio:** https://mnxx29.github.io/omnifish-wallpaper/

## Uso

1. Completa el nombre del centro y la empresa.
2. Elige la resolución del PC de destino.
3. Ajusta la calidad del JPG si lo necesitas. La vista previa muestra el peso real.
4. Descarga el JPG y envía solamente esa imagen por AnyDesk al equipo correspondiente.
5. Guarda el JPG en una carpeta fija del equipo y establécelo como fondo de escritorio.

La calidad inicial es 85 %. El ejemplo CERMAQ / Estero Conche a 1920 × 1080 ocupa aproximadamente 257 KB. El peso depende del texto, resolución y calidad elegidos.

## Funcionamiento

- HTML, CSS y JavaScript sin dependencias ni proceso de compilación.
- Toda la generación ocurre en el navegador mediante Canvas.
- Los nombres ingresados no se envían a un servidor ni se guardan.
- El fondo está incluido dentro de `index.html`. Se puede descargar ese archivo y abrirlo con Edge o Chrome para utilizar el generador sin conexión.
- Se conserva la proporción del fondo. En pantallas con otra proporción aparecen márgenes oscuros para evitar recortar o deformar la imagen.
- El fondo original mide 2752 × 1536 píxeles. Exportar a una resolución superior no añade detalle fotográfico, aunque el texto se genera a la resolución elegida.

## Desarrollo local

Abre `index.html` en el navegador. Para servirlo con un servidor local, opcionalmente ejecuta:

```sh
python -m http.server 8000
```

Visita `http://localhost:8000`.

## Publicación

GitHub Pages publica la raíz de la rama `main`. El archivo `.nojekyll` permite servir directamente los archivos estáticos. Los cambios enviados a `main` se publican automáticamente.

```sh
git add index.html README.md
git commit -m "Actualiza el generador de fondos"
git push
```

## Archivos

- `index.html`: aplicación completa con la imagen original incluida.
- `.nojekyll`: publicación estática en GitHub Pages.
- `.gitignore`: exclusiones de archivos locales y temporales.

## Recursos gráficos

El fondo y el logo provienen de la plantilla entregada por Omnifish. Este repositorio no otorga una licencia adicional sobre las marcas ni el material gráfico.
