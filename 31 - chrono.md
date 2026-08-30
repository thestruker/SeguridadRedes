How to automate tasks to run at intervals on linux servers?
Use ssh to connect to this server:

`Server: saturn.picoctf.net Port: 49235 Username: picoplayer Password: ENAFb6zfzn`
## Solución
```
dastruker-academy@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 49235
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.17.0-1019-aws x86_64)
```
```
picoplayer@challenge:~$ ls -la
total 12
drwxr-xr-x 1 picoplayer picoplayer   20 Aug 30 04:55 .
drwxr-xr-x 1 root       root         24 Aug  4  2023 ..
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Aug 30 04:55 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_1d781160}
```

## Notas Adicionales
cron es un sistema para automatizar comandos o programas

## Referencias
https://www.redhat.com/en/blog/linux-cron-command