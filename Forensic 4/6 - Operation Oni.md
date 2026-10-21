Download this disk image, find the key and log into the remote machine.
## Solución
Lancé la instancia para obtener el enlace del disco y los datos del SSH (ssh -i key_file -p <puerto> ctf-player@<host>). Descargué disk.img.gz en el webshell (en /tmp), lo descomprimí y con mmls vi que la partición raíz Linux empieza en el sector 206848. Busqué archivos de SSH con fls -r y en root/.ssh/ estaban id_ed25519 y id_ed25519.pub. Extraje la llave privada con icat, le puse permisos 600 y la usé para conectarme a la máquina remota como ctf-player. En el home estaba flag.txt:

academy{k3y_5l3u7h_0e000cd7}
## Notas Adicionales
- Comandos: fls -r -p -o 206848 disk.img | grep 'root/.ssh' ; icat -o 206848 disk.img <inodo id_ed25519> > key_file ; chmod 600 key_file ; ssh -i key_file -p <puerto> ctf-player@<host> 'cat flag.txt'
## Referencias
