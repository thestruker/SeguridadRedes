Can you find the flag in this disk image? This time I deleted the file!
## Solución
Descargué disko-4.dd.gz y lo descomprimí. fsstat mostró que es FAT32. Listé solo los archivos borrados con fls -r -d -p y aparecieron log/messages y log/dont-delete.gz (inodo 532021). En FAT los datos de un archivo borrado siguen en disco hasta que se sobrescriben, así que lo recuperé con icat, era un gzip, y al descomprimirlo decía "Here is your flag":

academy{d3l_d0n7_h1d3_w3ll_0a4d31fa}
## Notas Adicionales
- Comandos: fls -r -d -p disko-4.dd ; icat disko-4.dd 532021 > dd.gz ; zcat dd.gz
## Referencias
