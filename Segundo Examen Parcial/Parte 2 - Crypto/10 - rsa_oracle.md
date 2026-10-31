Can you abuse the oracle? ... The oracle can decrypt anything except the password.
## Solución
Lancé la instancia. El oráculo cifra y descifra con RSA pero se niega a descifrar el password. Usé la propiedad homomórfica de RSA: pedí cifrar el byte 0x02 (c2 = 2^e mod n), multipliqué c2 por el password cifrado y le pedí al oráculo descifrar ese producto: obtuve 2*password. Dividiendo entre 2 salió el password "20373". Con él descifré secret.enc usando openssl enc -aes-256-cbc -d -k 20373:

academy{su((3ss_(r@ck1ng_r3@_20373ec2}
## Notas Adicionales
- Ataque de texto cifrado elegido: (c_pass * 2^e)^d = 2*m mod n.
## Referencias
