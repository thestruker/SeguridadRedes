Files can always be changed in a secret way. Can you find the flag? cat.jpg
## Solución
Descargué cat.jpg; la imagen en sí no mostraba nada raro, así que revisé sus metadatos con exiftool. En el bloque XMP, el campo License (cc:license) tenía una cadena que no parecía una licencia normal: YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9. Por el alfabeto y la terminación se notaba que era Base64; al decodificarla salió la flag:

academy{the_m3tadata_1s_modified}
## Notas Adicionales
- Comandos: exiftool cat.jpg | grep -i license ; echo <cadena> | base64 -d
## Referencias
