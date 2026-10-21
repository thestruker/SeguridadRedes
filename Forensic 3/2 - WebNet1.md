We found this packet capture and key. Recover the flag.
## Solución
Igual que en WebNet0: descargué webnet1-capture.pcap y picopico.key, el tráfico era TLS con RSA key exchange y lo descifré cargando la llave privada en Wireshark (RSA keys list, puerto 443, http). Esta vez el header "Pico-Flag" de las respuestas era un señuelo (academy{this.is.not.your.flag.anymore}). Exporté los objetos HTTP (File → Export Objects → HTTP) y salieron second.html, starter-template.css, favicon.ico y vulture.jpg. Revisando los metadatos EXIF de vulture.jpg, el campo Artist contenía la flag:

academy{honey.roasted.peanuts}
## Notas Adicionales
- Comandos: tshark -r webnet1-capture.pcap -o "tls.keys_list:any,443,http,picopico.key" --export-objects http,salida ; luego exiftool salida/vulture.jpg
- La flag del header era falsa; la real estaba escondida en los metadatos de la imagen transferida.
## Referencias
