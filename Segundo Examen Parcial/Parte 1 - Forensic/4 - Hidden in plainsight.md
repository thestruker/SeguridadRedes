You're given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file.
## Solución
Descargué img.jpg y revisé sus metadatos con exiftool. El campo Comment tenía c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9, que en Base64 es "steghide:cEF6endvcmQ="; la segunda parte vuelta a decodificar da la contraseña "pAzzword". Con eso extraje el contenido oculto con steghide (steghide extract -sf img.jpg -p pAzzword) y salió flag.txt:

academy{h1dd3n_1n_1m4g3_7ba83d11}
## Notas Adicionales
- Pista doble: el comentario dice qué herramienta usar (steghide) y cuál es la contraseña, ambas en Base64.
## Referencias
