---
title: "¿Cómo crear un blog con Obsidian y Jekyll"
---

## ¿Cómo se creó este blog?
- Todos los artículos se escriben en formato `.md` (markdown).
- Se utiliza obsidian para escreibir de manera offline.
- Los archivos se guardan en [este repositorio](https://github.com/Miguel-Huaman/jekyll-obsidian).

## Consideraciones para escribir
- El título del artículo será el mismo que el archivo `.md`
- Jekyll no reconoce ciertos caracteres y solamente capitaliza la primera letra. Si un archivo contiene únicamente mayúsculas, solamente la primera letra se considerará así, el resto se convertirá a minúsculas.
- Cuando se necesiten títulos con caracteres especiales, es recomendable utilizar el fomarto xml. Ejemplo:
	```
	title: "¡Título con caracteres especiales!"
	```
- Las etiquetas, tags o hashtags `#` no están habilitados. Es recomendable siempre enlazar con corchetes o square brackets `[[ ]]`.