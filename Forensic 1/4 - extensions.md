This is a really weird text file. Can you find the flag? Get the flag from TXT.
## Solución
Descargué el archivo flag.txt, pero al revisar su tipo real con file (y su cabecera) resultó que no era texto sino una imagen PNG con la extensión cambiada. Le cambié la extensión a .png y al abrirla se veía la flag escrita dentro de la imagen:

academy{now_you_know_about_extensions}
## Notas Adicionales
- La cabecera del archivo empezaba con la firma de PNG, por eso no se abría como texto.
## Referencias
