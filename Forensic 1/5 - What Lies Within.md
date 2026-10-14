There's something in the building. Can you retrieve the flag?
## Solución
Descargué la imagen buildings.png. Como el reto apunta a esteganografía, extraje los bits menos significativos (LSB) de los canales RGB de la imagen (lo mismo que hace zsteg) y al decodificar esos bits apareció la flag escondida:

academy{h1d1ng_1n_th3_b1t5}
## Notas Adicionales
- La flag estaba oculta en el LSB de los canales RGB; se obtiene con zsteg o extrayendo el bit 0 de cada canal.
## Referencias
