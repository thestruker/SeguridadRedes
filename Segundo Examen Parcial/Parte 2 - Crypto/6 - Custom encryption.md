Can you get sense of this code file and write the function that will decode the given encrypted file content.
## Solución
custom_encryption.py hace dos pasos: 1) XOR del texto invertido con la llave "trudeau"; 2) multiplica cada carácter por shared_key*311, donde shared_key es un Diffie-Hellman con p=97, g=31 y los valores a=87, b=22 que vienen en enc_flag. Calculé shared_key = (g^b mod p)^a mod p, dividí cada número del cifrado entre shared_key*311, hice XOR con "trudeau" y volteé la cadena:

academy{custom_d2cr0pt6d_b1f6d02d}
## Notas Adicionales
- La función inversa: chr(c // (key*311)) → XOR con la llave → invertir el orden.
## Referencias
