The service gives N, e and the RSA-encrypted flag.
## Solución
El servicio entrega N, e y el flag cifrado por RSA. El nombre del reto ("EVEN RSA") y las pistas delatan que N es par, así que uno de sus factores primos es 2. La factorización es trivial: p=2, q=N//2. Con eso calculé phi=(p-1)*(q-1)=q-1, d = inverso de e módulo phi, y descifré m = c^d mod N:

academy{tw0_1$_pr!m3207f407f}
## Notas Adicionales
- p=2; q=N//2; phi=q-1; d=pow(e,-1,phi); m=pow(c,d,N).
- RSA se rompe si se puede factorizar N; aquí 2 es un factor obvio.
## Referencias
