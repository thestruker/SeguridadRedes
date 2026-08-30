I accidentally wrote the flag down. Good thing I deleted it!
## Solución
```
dastruker-academy@webshell:~$ unzip challenge.zip
dastruker-academy@webshell:~/drop-in$ ls
message.txt
dastruker-academy@webshell:~/drop-in$ cat message.txt 
TOP SECRET
dastruker-academy@webshell:~/drop-in$ git log

dastruker-academy@webshell:~/drop-in$ git show 3d5ec8a26ee7b092a1760fea18f384c35e435139:message.txt

```

## Notas Adicionales
git log muestra el historial de commits dentro del repo