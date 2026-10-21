How about some hide and seek? Download this file here.
## Solución
Descargué unknown.zip, que contenía ukn_reality.jpg. La imagen no mostraba nada útil, así que revisé los metadatos con exiftool. El campo Attribution URL (cc:attributionURL del XMP) tenía la cadena YWNhZGVteXtNRTc0RDQ3QV9ISUREM05fYWViZThjMGZ9Cg==, que es Base64. Decodificándola salió la flag:

academy{ME74D47A_HIDD3N_aebe8c0f}
## Notas Adicionales
- Comandos: exiftool ukn_reality.jpg | grep -i attribution ; echo <cadena> | base64 -d
## Referencias
