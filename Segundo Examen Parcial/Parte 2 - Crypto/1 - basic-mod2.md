Take each number mod 41 and find the modular inverse for the result. Then map to the following character set: 1-26 are the alphabet, 27-36 are the decimal digits, and 37 is an underscore.
## Solución
Descargué message.txt con una lista de números. Para cada número calculé n mod 41 y luego su inverso modular módulo 41 (pow(x,-1,41) en Python), y mapeé el resultado al alfabeto indicado (1-26 letras, 27-36 dígitos, 37 guion bajo). Envolví el mensaje en el formato:

academy{1nv3r53ly_h4rd_fed0a735}
## Notas Adicionales
- Inverso modular: el número y tal que (x*y) mod 41 = 1.
## Referencias
