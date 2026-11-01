Interactive RSA quiz over nc. (cuestionario sobre los fundamentos de RSA)
## Solución
Me conecté con nc a la instancia. Es un cuestionario: en cada pregunta el servidor da ciertos parámetros y pide calcular otro, preguntando "IS THIS POSSIBLE and FEASIBLE? (Y/N)". Automaticé las respuestas con un script que, según lo que piden, calcula:
- p,q -> n = p*q
- n,p -> q = n//p
- p,q -> totient = (p-1)(q-1)
- e,p,q -> d = inverso de e mod phi
- plaintext,e,n -> c = m^e mod n
- ciphertext,e,n,p -> plaintext = c^d mod n (sacando q=n//p, phi, d)
Y responde "N" a lo imposible (factorizar n de 2048 bits solo con e,n; o descifrar sin la clave privada). Al final el servidor dice que convierta el último plaintext (de entero a bytes) para obtener la flag:

academy{wA8_th4t$_ill3aGal..oCfEd0082}
## Notas Adicionales
- Repasa qué se puede calcular en RSA con la clave pública y qué no (factorizar n es el problema duro).
- El último plaintext descifrado, pasado de número a ASCII, es la flag.
## Referencias
