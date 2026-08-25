Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/a35dc624cfda858ed12a4bce57f832dad3b433bad6cde2b98e25fae4bc8ff760/strings) without running it?

## Solución
```
dastruker-academy@webshell:~$ cat strings.1 | grep pico       
grep: (standard input): binary file matches
dastruker-academy@webshell:~$ string strings.1 | grep pico
-bash: string: command not found
dastruker-academy@webshell:~$ strings strings.1 | grep pico
picoCTF{5tRIng5_1T_60eA8fdA}
```

## Notas Adicionales
strings extraer cadenas a partir de binarios