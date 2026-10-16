# geochile-vectores

Unidades geológicas (polígonos) y fallas de las geodatabases (GDB) oficiales de SERNAGEOMIN, en JSON por carta, para el
[Visor GeoChile](https://cvenegas-sernageomin.github.io/GeoChile/). No es un producto oficial de SERNAGEOMIN: son los datos
de las GDB publicadas, simplificados (~40 m) para verse en el navegador.

- `index.json` — cartas (bounds, conteos, tamaño) y valores de cada filtro.
- `cartas/<id>.json` — una carta: `u` unidades (c código, n nombre, d definición, a ambiente, lc/lr litología **inferida del texto**, mx/mn edad en Ma, ep épocas que toca), `p` polígonos `[unidad, tipo, coordenadas]`, `ft` tipos de falla, `f` fallas `[tipo, nombre, observada(1)/inferida(2), manteo, tipo geom, coordenadas]`.
- `ingesta.json` — informe de la generación (cartas, datum corregido, % sin edad / sin litología).

Se genera con `tools/exportar_vectores.py` del repo GeoChile. Detalle y reglas (datum de GB-83/94/106/115) en su `CLAUDE.md`.
