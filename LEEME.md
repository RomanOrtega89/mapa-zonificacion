# Zonas de cobertura -- sitio publico

Carpeta lista para publicar en GitHub Pages. No necesita servidor ni base de
datos: son archivos estaticos.

## Publicar por primera vez

1. Crea un repositorio en GitHub (puede ser privado si tu organizacion lo
   permite; con GitHub Pages privado hace falta plan de pago, con repositorio
   publico es gratis y estos datos no son confidenciales).
2. Copia todo el contenido de esta carpeta a la raiz del repositorio.
3. `git add . && git commit -m "Zonas de cobertura" && git push`
4. En GitHub: Settings -> Pages -> Source: `Deploy from a branch`,
   Branch: `main` / `/ (root)`. Guarda.
5. En un par de minutos queda en `https://<usuario>.github.io/<repositorio>/`

## Actualizar

Vuelve a generar el sitio desde la aplicacion y repite el `git add/commit/push`.
Solo cambian los archivos de `datos/`.

## Enlace directo al taller

Se le puede mandar a cada taller su propia liga:

    https://<usuario>.github.io/<repositorio>/?taller=<id>

Los ids estan en `datos/indice.json`, y la aplicacion los lista al generar.

## Que contiene

- `index.html` -- la pagina completa (mapa, buscador, lista, descarga CSV)
- `leaflet.js` / `leaflet.css` -- la libreria del mapa, incluida para no
  depender de un CDN externo
- `datos/` -- los datos generados
- `.nojekyll` -- evita que GitHub procese la carpeta con Jekyll
