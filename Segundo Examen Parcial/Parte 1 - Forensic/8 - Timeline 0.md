Can you find the flag in this disk image? Wrap what you find in the academy{} flag format.
## Solución
Descargué partition4.img.gz en el webshell y lo descomprimí (es una partición ext4 de Alpine). Como el reto se llama Timeline, generé la línea de tiempo con fls -r -m / partition4.img > body y ordené los archivos por fecha de modificación. Casi todo era de 2021-2025, pero /bin/bcab tenía fechas de 1985-01-01 (timestomping, alguien alteró las fechas para esconderlo). Su contenido (41 bytes) era Base64: NzFtMzExbjNfMHU3MTEzcl9oM3JfNDNhMmU3YWYK → 71m311n3_0u7113r_h3r_43a2e7af. Envolviéndolo en el formato:

academy{71m311n3_0u7113r_h3r_43a2e7af}
## Notas Adicionales
- Comandos: fls -r -m / partition4.img > t0.body ; awk -F'|' '{print $9,$2}' t0.body | sort -n | head ; icat partition4.img 4945 | base64 -d
- El archivo raro destaca por ser el más "viejo" del sistema (outlier en la línea de tiempo).
## Referencias
