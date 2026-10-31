The SOC team discovered a suspiciously large log file... they found an enormous block of encoded text instead of typical logs.
## Solución
Descargué logs.txt (1.5 MB). Empezaba con iVBORw0KGgo, que es la cabecera de un PNG codificado en Base64. Lo decodifiqué a un archivo .png y salió una imagen de un hacker; en la parte de abajo había una cadena en hexadecimal: 61636164656D797B...7D. Convirtiendo ese hex a ASCII salió la flag:

academy{forensics_analysis_is_amazing_8dbd3133}
## Notas Adicionales
- Comandos: base64 -d logs.txt > out.png ; luego echo <hex> | xxd -r -p
## Referencias
