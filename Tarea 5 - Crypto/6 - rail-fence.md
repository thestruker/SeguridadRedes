message.txt
## Solución
Descargué message.txt: "Ta _7N6D4Chlg:W3D_H3C31N__3E4ef sHR053F38N43DBC i33___NB". Es un cifrado de transposición Rail Fence: el texto se escribe en zigzag sobre varios rieles y se lee fila por fila. Probando con 4 rieles, reconstruí el patrón zigzag (periodo 2*(4-1)=6), repartí los caracteres en cada riel según cuántos le tocan y leí en orden:

academy{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_43BBCEC4}
## Notas Adicionales
- No cambia las letras, solo su orden (transposición). La clave es el número de rieles (4).
## Referencias
