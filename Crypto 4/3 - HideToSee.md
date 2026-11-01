atbash.jpg
## Solución
Descargué atbash.jpg. El nombre del archivo da dos pistas: hay algo escondido con esteganografía y el cifrado es Atbash. Primero extraje el texto oculto con steghide (sin contraseña):

steghide extract -sf atbash.jpg -p "" -xf output.txt

Salió zxzwvnb{zgyzhs_xizxp_zz003u7z}, que está cifrado con Atbash (cada letra se reemplaza por su espejo en el alfabeto: a↔z, b↔y, ...). Aplicando Atbash:

academy{atbash_crack_aa003f7a}
## Notas Adicionales
- Atbash: chr(ord('z') - (ord(c) - ord('a'))) para minúsculas. Es su propio inverso.
## Referencias
