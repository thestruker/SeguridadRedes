We found this file. Recover the flag.
## Solución
Descargué el archivo c0rrupt-mystery. Al revisar su cabecera con un editor hexadecimal vi que la firma del archivo estaba dañada; en realidad era un PNG con los bytes corrompidos. Reparé la firma PNG (89 50 4E 47 0D 0A 1A 0A) y el tipo del chunk IHDR. El framing del primer chunk IDAT también estaba dañado, pero el stream comprimido (zlib) estaba intacto, así que reensamblé los segmentos IDAT (los siguientes eran de 65524 bytes), descomprimí los datos y reconstruí la imagen con las dimensiones del IHDR (1642x1095, RGB). Al renderizarla apareció la flag escrita sobre un fondo rojo:

academy{c0rrupt10n_1847995}
## Notas Adicionales
- Firma PNG correcta: 89 50 4E 47 0D 0A 1A 0A.
- La clave fue que los datos comprimidos (zlib, cabecera 78 5E) seguían intactos aunque el framing de los chunks estaba roto.
## Referencias
