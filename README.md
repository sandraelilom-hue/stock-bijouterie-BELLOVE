# stock-bijouterie (Frolitas) - GitHub Pages deploy

Este repo contiene una **página estática** (index.html) para gestionar el stock de accesorios de bijouterie.
La página funciona offline y guarda los cambios en el navegador (localStorage).

---

## Archivos incluidos
- `index.html` : la aplicación web (HTML + CSS + JavaScript).
- `example_stock.json` : ejemplo de archivo JSON que podés subir con el botón *Cargar JSON*.
- `README.md` : este archivo con instrucciones.

---

## Paso a paso para publicar en GitHub Pages (vía web UI)

1. Iniciá sesión en https://github.com/ (o creá una cuenta).
2. Hacé clic en **New repository**.
   - Nombre: `stock-bijouterie` (podés cambiarlo).
   - Seleccioná **Public**.
   - No necesitas inicializar con README (ya viene en este zip).
3. En la página del repo nuevo hacé clic en **Add file → Upload files**.
   - Arrastrá `index.html`, `README.md` y `example_stock.json` desde tu computadora.
   - Commit: escribí un mensaje (por ejemplo: "Initial commit") y hacé clic en **Commit changes**.
4. Hacé clic en la pestaña **Settings** del repositorio.
5. En el menú lateral buscá **Pages** (o "Pages" dentro de "Code and automation").
6. En **Build and deployment** / **Source**, seleccioná la rama `main` (o `master`) y la carpeta `/ (root)`.
7. Guardá los cambios. GitHub mostrará la URL pública (algo como `https://tuusuario.github.io/stock-bijouterie/`).

> Abrí esa URL en tu iPhone con Safari. Para ponerla en el Home Screen: tocá el botón Compartir → *Add to Home Screen* (Agregar a pantalla de inicio).

---

## Alternativa: subir con Git (línea de comandos)

Desde la carpeta donde están los archivos:

```bash
# Renombrar el archivo HTML a index.html si hace falta
mv stock_bijouterie_fixed.html index.html

git init
git add index.html README.md example_stock.json
git commit -m "Initial commit"
git branch -M main
# reemplazá <tuusuario> y <repo> por los reales
git remote add origin https://github.com/<tuusuario>/stock-bijouterie.git
git push -u origin main
```

Después andá a **Settings → Pages** y seleccioná main / root.

---

## Notas & Troubleshooting

- **Nombre del archivo**: GitHub Pages busca `index.html` en la raiz del repo. Asegurate que el `index.html` esté en la carpeta raíz.
- **Privacidad**: hacelo **público** para evitar posibles restricciones al desplegar Pages.
- **localStorage**: los datos se guardan en el navegador del usuario. No se sincronizan entre dispositivos. Si querés sincronización necesitas una solución con servidor o almacenamiento en la nube.
- **Probar JSON**: usá `example_stock.json` para probar la carga desde el botón *Cargar JSON*.
- **Actualizar la página**: cada vez que subas cambios hacé commit/push; luego recargá la URL en el navegador para verlos.

---

Si querés, yo subo los archivos a un repo de ejemplo en GitHub por vos (necesitaría que me compartas acceso o token), o te doy los comandos exactos para tu sistema. Decime cómo preferís proceder, Vale.
