Unzip this archive and find the file named 'uber-secret.txt'

## Solución
```
dastruker-academy@webshell:~/files$ ls
13771.txt.utf-8  acceptable_books  satisfactory_books
14789.txt.utf-8  adequate_books
dastruker-academy@webshell:~/files$ ls
13771.txt.utf-8  acceptable_books  satisfactory_books
14789.txt.utf-8  adequate_books
dastruker-academy@webshell:~/files$ ls -a
.   13771.txt.utf-8  acceptable_books  satisfactory_books
..  14789.txt.utf-8  adequate_books
dastruker-academy@webshell:~/files$ cd adequate_books/
dastruker-academy@webshell:~/files/adequate_books$ ls -a
.  ..  44578.txt.utf-8  46804-0.txt  more_books
dastruker-academy@webshell:~/files/adequate_books$ cd more_books/
dastruker-academy@webshell:~/files/adequate_books/more_books$ ls -a
.  ..  .secret  1023.txt.utf-8
dastruker-academy@webshell:~/files/adequate_books/more_books$ cd .secret/
dastruker-academy@webshell:~/files/adequate_books/more_books/.secret$ ls -a
er_secrets/cademy@webshell:~/files/adequate_books/more_books/.secret$ cd deepe
dastruker-academy@webshell:~/files/adequate_books/more_books/.secret/deeper_s
ecrets$ ls -a
.  ..  deepest_secrets
dastruker-academy@webshell:~/files/adequate_books/more_books/.secret/deeper_s
ecrets$ cd deepest_secrets/
dastruker-academy@webshell:~/files/adequate_books/more_books/.secret/deeper_s
ecrets/deepest_secrets$ ls -a
.  ..  uber-secret.txt
dastruker-academy@webshell:~/files/adequate_books/more_books/.secret/deeper_s
ecrets/deepest_secrets$ cat uber-secret.txt 
picoCTF{f1nd_15_f457_ab443fd1}
```

## Notas Adicionales
ls -a revisa hasta archivos ocultos