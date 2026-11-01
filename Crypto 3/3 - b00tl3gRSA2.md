Connect to the service to get c, n and e. (RSA de contrabando)
## Solución
Me conecté con nc a la instancia y me dio c, n y un exponente e enorme (del tamaño de n). Eso es sospechoso: en RSA normal e es chico (65537) y d es grande. Aquí el autor cifró usando d en vez de e (c = m^d mod n). Por la simetría de RSA, basta "cifrar" de nuevo el criptograma con el exponente estándar e=65537 para recuperar el mensaje: m = c^65537 mod n:

academy{bad_1d3a5_8722867}
## Notas Adicionales
- Cifrar con d y descifrar con e es equivalente a cifrar con e y descifrar con d; (m^d)^e = m mod n.
- Comando: conectar por nc, parsear c/n y m=pow(c,65537,n).
## Referencias
