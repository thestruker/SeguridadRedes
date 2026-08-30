Can you read files in the root file?

## Solución
```
dastruker-academy@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 60306 
The authenticity of host '[saturn.picoctf.net]:60306 ([13.59.203.175]:60306)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:60306' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.17.0-1019-aws x86_64)
```
```
dastruker-academy@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 60306 
The authenticity of host '[saturn.picoctf.net]:60306 ([13.59.203.175]:60306)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:60306' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.17.0-1019-aws x86_64)
```
```
# cat /root/.flag.txt
picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}
```
## Notas Adicionales

sudo para ejecutar en admin
-la muestra todos los archivos en su formato completo, incluyendo usuario