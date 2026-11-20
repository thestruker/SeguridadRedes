The name of the game is speed. Are you quick enough to solve this problem and keep it above 50 mph? (need-for-speed)
## Solución
El binario descifra la bandera en memoria, pero pone un temporizador con alarm(): si el cálculo de la clave (calculate_key) tarda demasiado, salta un manejador que imprime "demasiado lento" y termina. En vez de pelear con el tiempo, analicé el binario estáticamente. calculate_key siempre devuelve el mismo valor 0xe7af057b (el bucle solo da vueltas para gastar tiempo). Con esa clave fija, decrypt_flag hace un XOR byte a byte del arreglo flag usando los bytes de la clave (e incrementa la clave cuando el índice es múltiplo que cumple i%3==2). Extraje los bytes iniciales de flag del binario (.data) y repliqué decrypt_flag en Python:

academy{Good job keeping bus #31326f14 speeding along!}
## Notas Adicionales
- La "velocidad" es solo un alarm(); la clave 0xe7af057b es constante, así que el reto se resuelve sin presión de tiempo analizando calculate_key y decrypt_flag.
- También funciona neutralizando alarm() (p. ej. con un LD_PRELOAD que lo haga no-op) para dejar terminar el binario.
## Referencias
