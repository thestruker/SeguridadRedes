Download the disk image and use mmls on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.
## Solución
Descargué disk.img.gz, lo descomprimí y corrí mmls disk.img para ver la tabla de particiones (DOS). Había una sola partición Linux (0x83) que empieza en el sector 2048 y tiene una longitud de 202752 sectores. Lancé la instancia, me conecté al checker con nc y respondí 202752 a la pregunta "What is the size of the Linux partition in the given disk image?". El servicio respondió "Great work!" con la flag:

academy{mm15_f7w!}
## Notas Adicionales
- Comandos: mmls disk.img ; nc <host> <puerto> (respuesta: 202752, la columna Length en sectores de 512 bytes).
## Referencias
