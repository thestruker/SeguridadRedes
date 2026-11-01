I have these 2 images, can you make a flag out of them? scrambled1.png scrambled2.png
## Solución
Descargué scrambled1.png y scrambled2.png; por separado solo se ven como ruido aleatorio. Es criptografía visual: cada imagen es una "parte" y hay que combinarlas. Sumé los valores RGB de ambas imágenes píxel por píxel módulo 256; al hacerlo el ruido se alinea y aparece el texto de la flag sobre fondo blanco:

academy{2f16d0c4}
## Notas Adicionales
- Script: con Pillow/NumPy, out = (img1 + img2) % 256 y guardar el resultado.
- Una sola imagen no revela nada; el secreto está repartido entre las dos (visual cryptography).
## Referencias
