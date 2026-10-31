Everything seems secure; strong numbers, familiar parameters but something small might ruin it all.
## Solución
encryption.py genera primos de 1048 bits pero elige d como un primo de solo 256 bits y calcula e = d^-1 mod phi. Cuando d < n^(1/4)/3, aplica el ataque de Wiener: con la expansión en fracciones continuas de e/n, uno de los convergentes k/d revela d. Probé cada convergente descifrando c y el que dio texto con "academy" fue el correcto:

academy{sm4ll_d_073963cb}
## Notas Adicionales
- Ataque de Wiener (exponente privado pequeño).
## Referencias
