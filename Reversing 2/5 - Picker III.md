Can you figure out how this program works to get the flag? (picker-III.py)
## Solución
Aquí ya no se puede llamar a cualquier función: el menú solo ejecuta las que están en una tabla de texto (func_table) con entradas de 32 caracteres. Pero existe la opción write_variable, que hace exec('global '+nombre+'; '+nombre+' = '+valor) con un filtro que solo prohíbe ';', '(' y ')'. Usé esa opción para sobreescribir la propia variable global func_table, poniendo 'win' como primera entrada (rellenada a 128 caracteres con espacios, usando 'win'+' '*125, que no tiene paréntesis). Después elegí la opción 1, que ejecuta la primera función de la tabla: ahora win():

academy{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_3350bb13}
## Notas Adicionales
- La protección (tabla de funciones permitidas) se rompe porque el usuario puede modificar esa misma tabla en memoria.
- Secuencia: write_variable -> func_table = 'win'+' '*125 -> opción 1.
## Referencias
