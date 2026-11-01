The service presents hashes to crack.
## Solución
El servicio da 3 hashes en secuencia, uno por algoritmo, que hay que crackear. El algoritmo se identifica por la longitud en hex: MD5 (32), SHA-1 (40), SHA-256 (64). Los dos primeros eran contraseñas comunísimas (password123, letmein) y el tercero lo crackeé por diccionario contra rockyou.txt (qwerty098). Al enviar las tres el servicio soltó la flag:

academy{UseStr0nG_h@shEs_&PaSswDs!_6bbfe014}
## Notas Adicionales
- Longitud del hash = pista del algoritmo. rockyou.txt para el de SHA-256.
## Referencias
