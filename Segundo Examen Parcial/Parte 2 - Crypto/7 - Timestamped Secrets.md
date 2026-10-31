Someone encrypted a message using AES in ECB mode... the key is derived from something as simple as the current time!
## Solución
message.txt dice que se cifró alrededor del timestamp 1790147510 y da el ciphertext en hex. Según encryption.py la llave es sha256(str(timestamp))[:16]. Probé timestamps alrededor de ese valor (fuerza bruta) descifrando con AES-ECB hasta que el texto empezara con "academy"; el timestamp exacto fue 1790147510:

academy{sa3S_sEc9t_57326579}
## Notas Adicionales
- Usar el tiempo como semilla de la llave es inseguro: el espacio de búsqueda es diminuto.
## Referencias
