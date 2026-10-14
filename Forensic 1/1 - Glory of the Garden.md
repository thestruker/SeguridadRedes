This file contains more than it seems. Get the flag from garden.jpg.
## Solución
Descargué la imagen garden.jpg y como el reto dice que el archivo contiene más de lo que aparenta, le apliqué strings para revisar las cadenas de texto que escondía. Casi al final del archivo estaba la flag en texto plano:

academy{more_than_m33ts_the_3y3ee53c6bc}
## Notas Adicionales
- Comando usado: `strings garden.jpg | grep academy`
## Referencias
