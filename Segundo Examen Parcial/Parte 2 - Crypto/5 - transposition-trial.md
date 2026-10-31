Our data got corrupted on the way here... every block of 3 got scrambled around! The first word seems to be three letters long.
## Solución
message.txt: "heTfl g as icaaemd{...}". En bloques de 3, "heT" debe ser "The", o sea el tercer carácter pasa al inicio: el orden real es (c3, c1, c2). Apliqué esa permutación a todos los bloques de 3 y quedó "The flag is academy{...}":

academy{7R4N5P051N6_15_3XP3N51V3_C1CBA2A2}
## Notas Adicionales
- Python: ''.join(s[i+2]+s[i]+s[i+1] for i in range(0,len(s),3))
## Referencias
