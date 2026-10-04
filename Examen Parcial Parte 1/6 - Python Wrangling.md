Python scripts are invoked kind of like programs in the Terminal... Can you run [ende.py](https://challenge-files.cylabacademy.net/library/a4f054dce4d90aca10ca6075cc2598da541e9acf11ed4a138b962ec69b442f05/ende.py) using [password.txt](https://challenge-files.cylabacademy.net/library/a4f054dce4d90aca10ca6075cc2598da541e9acf11ed4a138b962ec69b442f05/password.txt) to get [flag.txt.en](https://challenge-files.cylabacademy.net/library/a4f054dce4d90aca10ca6075cc2598da541e9acf11ed4a138b962ec69b442f05/flag.txt.en)?
## Solución
Primero leí el contenido del archivo de la contraseña usando el comando `cat`:

```
dastruker-academy@webshell:~$ cat password.txt
563e47ddeaf84eca8b2a31201381a898
```

Luego ejecuté el script de Python en modo desencriptación pasándole el archivo cifrado como argumento:

```
dastruker-academy@webshell:~$ python3 ende.py -d flag.txt.en
Please enter the password:563e47ddeaf84eca8b2a31201381a898
academy{4p0110_1n_7h3_h0us3_d6af8f37}
```

Al ingresar la contraseña obtenida, el script descifró el archivo y me entregó la flag directamente en la pantalla:

`academy{4p0110_1n_7h3_h0us3_d6af8f37}`

## Notas Adicionales


## Referencias
