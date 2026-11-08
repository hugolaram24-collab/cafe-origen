# CAFÉ ORIGEN

Web estática de una cafetería ficticia, creada como segundo proyecto de portfolio para Malt. El menú, los precios y los horarios son de ejemplo. El correo usa el dominio reservado `.example` y se muestra como texto porque no hay buzón ni servicio de reservas. Las ilustraciones SVG son recursos locales creados para este proyecto.

## 1. Abrir el proyecto en VS Code

1. Descarga y descomprime `cafe-origen.zip`.
2. Abre Visual Studio Code y selecciona **Archivo → Abrir carpeta**. Elige la carpeta que contiene `index.html`.
3. Abre `index.html` en el navegador con doble clic desde el Explorador de archivos. La web funciona sin instalar paquetes ni extensiones.
4. Edita un archivo, guarda con **Ctrl+S** y recarga el navegador para ver el cambio.

## 2. Entender los archivos

```text
cafe-origen/
├── index.html
├── styles.css
├── README.md
└── assets/
    ├── grano.svg
    ├── cafe.svg
    ├── horno.svg
    └── rincon.svg
```

1. **HTML define el contenido.** `header` contiene la cabecera, `nav` agrupa los enlaces, `main` reúne el contenido y `footer` cierra la página. El título principal usa `h1`, y cada sección tiene un `h2`.
2. **Los enlaces internos saltan a una sección.** Al pulsar Carta, `href="#carta"` busca el elemento que tiene `id="carta"`. Si cambias el identificador, actualiza los enlaces que lo usan.
3. **CSS define el aspecto.** La etiqueta `link` del HTML carga `styles.css`. Las variables de `:root` guardan los colores. Por ejemplo, cambia `--crema` para probar otro fondo y comprueba que el texto siga siendo legible.
4. **Flexbox y Grid ordenan los elementos.** Flexbox distribuye la marca y la navegación. Grid crea las columnas de la portada, la carta y la galería. La regla `@media (max-width: 43rem)` apila esas columnas en pantallas estrechas.
5. **Las imágenes usan rutas relativas.** `assets/horno.svg` significa «entra en la carpeta assets junto a index.html». Los textos `alt` describen las imágenes de la galería. La imagen decorativa de portada usa `alt=""` para evitar repetir esa descripción.

Para practicar, cambia un precio dentro de `class="productos"`, guarda y recarga. Luego cambia el ancho de la ventana y observa cómo se reorganizan las categorías.

## 3. Publicar en GitHub Pages

1. Crea un repositorio público en GitHub llamado `cafe-origen`.
2. En **Add file → Upload files**, sube `index.html`, `styles.css`, `README.md` y la carpeta `assets` con sus cuatro SVG. Si el repositorio está vacío, GitHub muestra un enlace para subir archivos en la pantalla inicial.
3. Guarda los cambios en la rama `main`. En la pestaña **Code**, comprueba que `index.html` y `assets` aparecen en el primer nivel del repositorio.
4. En **Settings → Pages**, selecciona **Deploy from a branch** como origen. Elige **main** y **/(root)**, y pulsa **Save**.
5. Abre el enlace que aparezca en **Settings → Pages** cuando termine el despliegue. Para un repositorio llamado `cafe-origen`, la URL habitual tiene la forma `https://TU-USUARIO.github.io/cafe-origen/`.

[Guía oficial de GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

## 4. Comprobar la web

- Abre la página y pulsa los cuatro enlaces de navegación, **Ver la carta** y **Volver arriba**.
- Pulsa **Tab** desde el inicio. Debe aparecer **Saltar al contenido** y el foco debe ser visible en los enlaces.
- En el navegador, pulsa **F12** y activa la vista de dispositivos para probar un ancho de 375 px. Comprueba que se leen los precios y que la página cabe sin desplazamiento horizontal.
- Si falta el estilo o una ilustración, comprueba que el archivo conserva su nombre en minúsculas y que `assets` sigue junto a `index.html`. Repite la comprobación en la URL publicada.