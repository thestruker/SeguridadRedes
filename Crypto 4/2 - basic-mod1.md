message.txt (una lista de números). Descífralo con aritmética modular.
## Solución
Descargué message.txt con una lista de números enteros. El esquema es: a cada número le aplico módulo 37, y mapeo el resultado a un conjunto de caracteres: 0-25 = letras A-Z, 26-35 = dígitos 0-9, 36 = guion bajo. Concatenando los caracteres y envolviendo en el formato:

academy{R0UND_N_R0UND_0686D44A}
## Notas Adicionales
- charset = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_'; result = ''.join(charset[n%37] for n in numbers)
## Referencias
