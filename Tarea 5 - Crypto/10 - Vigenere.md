cipher.txt
## Solución
Descargué cipher.txt: caldfow{O0NU_WQ3_G1G3O3T3_A1AH3S_4c372077}. Tiene forma de flag pero el prefijo está cifrado con Vigenere. Probando que "caldfow" descifre a "academy" salió la clave CYLAB (5 letras, se repite cíclicamente). Descifrando todo con P_i = (C_i - K_i) mod 26 (sin tocar dígitos ni símbolos):

academy{D0NT_US3_V1G3N3R3_C1PH3R_4a372077}
## Notas Adicionales
- Clave: CYLAB. Vigenere es polialfabético: cada letra se desplaza según la letra correspondiente de la clave.
## Referencias
