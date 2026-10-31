Can you find the flag in this disk image? Wrap what you find in the academy{} flag format.
## Solución
Igual que Timeline 0: descomprimí timeline-1-partition4.img.gz, generé el body file con fls -r -m / y ordené por fecha. Esta vez no había fechas viejas falsas; el archivo sospechoso estaba entre los últimos modificados, junto con el arranque: /etc/chat (49 bytes, inodo 32716), que no es un archivo normal de Alpine. Su contenido era Base64: NTczNDE3aDEzcl83aDRuXzdoM18xNDU3XzU4NTI3YmIyMjIK → 573417h13r_7h4n_7h3_1457_58527bb222 ("stealthier than the last"). En formato:

academy{573417h13r_7h4n_7h3_1457_58527bb222}
## Notas Adicionales
- Comandos: fls -r -m / img > t1.body ; awk -F'|' '{print $9,$3,$2}' t1.body | sort -n | tail ; icat img 32716 | base64 -d
## Referencias
