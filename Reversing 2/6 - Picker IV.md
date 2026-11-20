Can you figure out how this program works to get the flag? (picker-IV, binario en C)
## Solución
Esta versión está en C. El programa pide una dirección en hexadecimal y salta a ejecutarla (jump a una dirección dada por el usuario). En el binario hay una función win() que lee e imprime flag.txt. Saqué su dirección del binario con nm (símbolo win) y se la pasé al servicio por nc, sin el prefijo 0x. Al saltar a esa dirección, el programa ejecuta win() e imprime la bandera:

academy{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_cd521e4c}
## Notas Adicionales
- Dirección de win: 0x4012a1 (obtenida con: nm picker-IV | grep win).
- Dejar que el usuario indique a qué dirección saltar es una vulnerabilidad clásica de control de flujo.
## Referencias
