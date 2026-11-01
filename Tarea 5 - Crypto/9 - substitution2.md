message.txt (texto más corto)
## Solución
Descargué message.txt, otra sustitución monoalfabética pero con texto más corto, donde el conteo simple de letras no basta. Afiné el ataque con análisis de n-gramas (bigramas y trigramas frecuentes como "the", "and", "ing") además de las frecuencias de letras, hasta recuperar el mapeo y leer la flag:

academy{N6R4M_4N41Y515_15_73D10U5_CFE4E232}
## Notas Adicionales
- Con poco texto, los n-gramas (pares/tripletes de letras) ayudan donde la frecuencia por letra falla.
## Referencias
