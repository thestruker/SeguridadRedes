Fix the syntax error in the Python script to print the flag.

## Solución
```
dastruker-academy@webshell:~$ python fixme2.py 
  File "/home/dastruker-academy/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
```
```
dastruker-academy@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```
## Notas Adicionales
'=' no es lo mismo a '==