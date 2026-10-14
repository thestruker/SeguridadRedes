Find the flag in this picture.
## Solución
Descargué la imagen pico_img.png. Como el nombre del reto (So Meta) apunta directamente a los metadatos, revisé la información del archivo con strings y encontré la flag guardada dentro de un chunk de texto de la imagen:

academy{s0_m3ta_b9d1ec99}
## Notas Adicionales
- La flag estaba embebida como metadato, se puede ver con `strings` o con exiftool.
## Referencias
