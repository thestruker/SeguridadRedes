We found this file. Recover the flag. tunn3l_v1s10n
## Solución
Descargué tunn3l_v1s10n, que no tenía extensión. Con un editor hexadecimal vi que empezaba con "BM", o sea que era un BMP, pero no abría porque la cabecera estaba alterada: el offset a los datos de píxeles (bytes 10-13) y el tamaño del encabezado DIB (bytes 14-17) estaban en 0xD0BA ("BAD0"). Los corregí a 54 (0x36) y 40 (0x28), que son los valores estándar. Con eso la imagen abrió, pero solo mostraba "NOT THE FLAG" (señuelo). La cabecera decía 1134x306 a 24 bits, pero el archivo pesaba mucho más: 2,893,400 bytes de píxeles / 3404 bytes por fila (1134*3 con padding) = 850 filas. Cambié la altura (bytes 22-25) de 306 a 850 y apareció la parte de arriba de la imagen con la flag:

academy{qu1t3_a_v13w_2020}
## Notas Adicionales
- Campos corregidos: bfOffBits = 54, biSize = 40, biHeight = 850.
- El texto de la flag se sale un poco de los bordes de la imagen, pero se reconstruye completo: academy{qu1t3_a_v13w_2020}.
## Referencias
