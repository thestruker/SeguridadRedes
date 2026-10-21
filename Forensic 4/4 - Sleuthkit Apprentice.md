Download this disk image and find the flag.
## Solución
Descargué disk.flag.img.gz y lo descomprimí. Con mmls vi tres particiones: una Linux en el sector 2048 (boot), una swap y otra Linux en el sector 360448 (la raíz). Listé recursivamente los archivos de la partición raíz con fls -r -p -o 360448 y filtré por "flag": aparecieron root/my_folder/flag.txt (borrado, realloc, contenido basura) y root/my_folder/flag.uni.txt (inodo 2371). Extraje este último con icat; estaba en texto UTF-16 (con bytes nulos entre caracteres), así que quité los nulos y salió la flag:

academy{by73_5urf3r_217f681f}
## Notas Adicionales
- Comandos: mmls disk.flag.img ; fls -r -p -o 360448 disk.flag.img | grep -i flag ; icat -o 360448 disk.flag.img 2371 | tr -d '\000'
## Referencias
