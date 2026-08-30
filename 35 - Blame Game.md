Someone's commits seems to be preventing the program from working. Who is it?

You can download the challenge files here:
## Solución
```
dastruker-academy@webshell:~$ cd drop-in/
dastruker-academy@webshell:~/drop-in$ ls
message.py
dastruker-academy@webshell:~/drop-in$ cat message.py 
print("Hello, World!"
dastruker-academy@webshell:~/drop-in$ git log
dastruker-academy@webshell:~/drop-in$ git blame message.py

23e9d4ce (picoCTF{@sk_th3_1nt3rn_81e716ff} 2024-03-12 00:07:15 +0000 1) print("Hello, World!"
```

## Notas Adicionales
git blame muestra que autor modifico cada alinea de un archivo