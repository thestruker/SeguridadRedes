We received an encrypted message. See if you can make sense of the numbers and reveal the flag. message.txt (n, e, c)
## Solución
Descargué message.txt con n, e=20 y c. La pista es que e es muy pequeño: si el mensaje m es chico, entonces m^e sigue siendo menor que n y nunca se reduce módulo n, así que c = m^e sin más. Para recuperar m basta sacar la raíz 20-ésima entera exacta de c (sin factorizar n):

academy{t1ny_e_227220c9}
## Notas Adicionales
- Raíz entera por búsqueda binaria; m = iroot(c, 20); luego m.to_bytes(...) para pasar a texto.
- Ataque de exponente público pequeño (low public exponent).
## Referencias
