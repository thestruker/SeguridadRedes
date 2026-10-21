Use srch_strings from the sleuthkit and some terminal-fu to find a flag in this disk image. dds1-alpine.flag.img.gz
## Solución
Descargué dds1-alpine.flag.img.gz y lo descomprimí con gunzip. Como pide el reto, usé srch_strings (de The Sleuth Kit) para sacar todas las cadenas de texto de la imagen de disco y las filtré con grep buscando el formato de la flag. Apareció dentro de un texto tipo "SAY ...":

academy{f0r3ns1c4t0r_n30phyt3_6502313d}
## Notas Adicionales
- Comando: srch_strings dds1-alpine.flag.img | grep -i 'academy{'
## Referencias
