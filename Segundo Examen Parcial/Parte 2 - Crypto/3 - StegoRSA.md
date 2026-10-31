A message has been encrypted using RSA. The public key is gone… but someone might have been careless with the private key.
## Solución
Descargué flag.enc e image.jpg. Con exiftool vi que el campo Comment de la imagen era una cadena hexadecimal larga; al pasarla de hex a texto salió una llave privada RSA completa (-----BEGIN PRIVATE KEY-----). Con esa llave descifré flag.enc (m = c^d mod n) y al final del bloque estaba la flag:

academy{rs4_k3y_1n_1mg_d97b7bfb}
## Notas Adicionales
- Comandos: exiftool -b -Comment image.jpg | xxd -r -p > key.pem ; openssl pkeyutl -decrypt -inkey key.pem -in flag.enc (o RSA en Python).
## Referencias
