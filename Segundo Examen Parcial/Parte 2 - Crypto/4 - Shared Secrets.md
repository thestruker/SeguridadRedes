A message was encrypted using a shared secret... but it looks like one side of the exchange leaked something.
## Solución
Es un intercambio Diffie-Hellman. message.txt da g, p, A (pública del servidor) y, por error, b (el secreto privado del cliente). Con eso el secreto compartido es shared = A^b mod p. Según encryption.py, la flag se cifró haciendo XOR de cada byte con (shared % 256). Repetí el XOR sobre enc y salió:

academy{dh_s3cr3t_5d9c8fbe}
## Notas Adicionales
- Python: shared = pow(A, b, p); bytes(x ^ (shared % 256) for x in enc)
## Referencias
