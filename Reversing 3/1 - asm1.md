What does asm1(0x31e) return? Submit the flag as a hexadecimal value (starting with '0x'). (test.S)
## Solución
El reto da el desensamblado de la función asm1 y pide el valor de retorno para la entrada 0x31e. Seguí el flujo del código: primero compara el argumento con 0x2fa; como 0x31e (798) es mayor, salta a la rama que compara contra 0x31e. Como coincide exactamente, ejecuta eax = arg - 0x17 (resta 23) y retorna. Entonces 0x31e - 0x17 = 0x307:

0x307
## Notas Adicionales
- No hace falta ejecutar: basta trazar los saltos condicionales (cmp/jg/jne) con el argumento dado.
- 798 - 23 = 775 = 0x307.
## Referencias
