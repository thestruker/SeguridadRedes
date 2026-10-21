Download this disk image and find the flag.
## Solución
Descargué disk.flag.img.gz y lo descomprimí. mmls mostró la partición raíz Linux en el sector 411648. Con fls -r busqué en ella y en /root había tres archivos interesantes: .ash_history, flag.txt (borrado) y flag.txt.enc. Leí el historial de la shell con icat y ahí estaba el comando exacto que usó el usuario para cifrar la flag:

openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567

y después hizo shred -u flag.txt. Extraje flag.txt.enc con icat y lo descifré con la misma contraseña usando openssl aes256 -d. Salió la flag:

academy{h4un71ng_p457_0b36d810}
## Notas Adicionales
- Comandos: fls -r -p -o 411648 disk.flag.img | grep -iE 'flag|ash_history' ; icat -o 411648 disk.flag.img <inodo> ; openssl aes256 -d -salt -in flag.txt.enc -k unbreakablepassword1234567
- openssl muestra advertencias (derivación de llave obsoleta / bad decrypt en el padding), pero el texto plano con la flag sale completo.
## Referencias
