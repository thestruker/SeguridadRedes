Can you figure out how this program works to get the flag? (picker-II.py)
## Solución
Es igual que Picker I pero ahora hay un filtro: si la cadena contiene la subcadena 'win' la rechaza. El eval sigue estando (eval(user_input + '()')), así que solo hay que llamar a win() sin escribir literalmente "win". Lo resolví construyendo el nombre por partes y buscándolo en el diccionario global: globals()['w'+'in'], que no contiene la subcadena "win" pero al evaluarse apunta a la función win y el programa le añade () y la ejecuta:

academy{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_c9aa7a3c}
## Notas Adicionales
- Un filtro por subcadena ('win' in input) es trivial de evadir; el problema de fondo sigue siendo el eval().
- Payload: globals()['w'+'in']
## Referencias
