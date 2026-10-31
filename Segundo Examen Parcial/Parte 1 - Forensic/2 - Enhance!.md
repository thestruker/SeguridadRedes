Download this image file and find the flag.
## Solución
Descargué drawing.flag.svg. Al abrirlo solo se ve un círculo, pero un SVG es XML, así que lo abrí como texto. Dentro había varios elementos <tspan> con tamaño de letra diminuto (invisibles en la imagen), cada uno con un pedazo de la flag. Uní el contenido de todos los <tspan> y quité los espacios:

academy{3nh4nc3d_5b5e6f18}
## Notas Adicionales
- Comando: grep -o '<tspan[^>]*>[^<]*' drawing.flag.svg y concatenar el texto.
## Referencias
