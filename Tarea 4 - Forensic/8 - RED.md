RED, RED, RED, RED. Download the image: red.png
## Solución
Descargué red.png, una imagen 128x128 completamente roja. Sus metadatos (chunk tEXt "Poem") traían un poema cuyas iniciales de cada verso forman "CHECKLSB", una pista para revisar los bits menos significativos. Extraje el LSB de los 4 canales (R, G, B y A) de cada píxel y salió una cadena Base64 repetida: YWNhZGVteXtyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==. Al decodificarla:

academy{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}
## Notas Adicionales
- zsteg red.png lo detecta como b1,rgba,lsb. Importante incluir el canal alfa.
## Referencias
