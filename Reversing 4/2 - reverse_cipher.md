We have recovered a binary and a text file. Can you reverse the flag. (rev, rev_this)
## Solución
El binario rev lee la bandera de flag.txt, le aplica una transformación y guarda el resultado en rev_this. Desensamblando main vi la lógica: los primeros 8 caracteres y el último se escriben sin cambio; para los caracteres de en medio (índices 8 a 22), si el índice es par le suma 5 y si es impar le resta 2. Para recuperar la flag hice la operación inversa sobre el contenido de rev_this (índices pares -5, impares +2) y verifiqué re-cifrando que coincidía exactamente con rev_this:

academy{r3v3rs354680934}
## Notas Adicionales
- La transformación es un cifrado por sustitución dependiente de la posición, totalmente reversible sin llave.
- Lo resolví y verifiqué con un script corto en Python leyendo los bytes exactos de rev_this.
## Referencias
