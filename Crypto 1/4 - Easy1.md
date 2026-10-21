The one time pad can be cryptographically secure, but not when you know the key. We've given you the encrypted flag, key, and a table: UFJKXQZQUNB with the key of SOLVECRYPTO.
## Solución
La tabla (table.txt) es una tabla de Vigenère (tabula recta). Para descifrar, por cada letra de la llave se busca la columna/fila correspondiente y la letra cifrada, o equivalentemente se calcula (cifrado - llave) mod 26 letra por letra:
U-S=C, F-O=R, J-L=Y, K-V=P, X-E=T, Q-C=O, Z-R=I, Q-Y=S, U-P=F, N-T=U, B-O=N → CRYPTOISFUN. Envolviéndolo en el formato de la flag:

academy{CRYPTOISFUN}
## Notas Adicionales
- Es un Vigenère/one-time-pad con llave conocida, por eso es trivial de romper.
## Referencias
