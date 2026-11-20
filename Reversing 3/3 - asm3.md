What does asm3(0xba75113d,0xdc9e1676,0xe2b51af6) return? Submit the flag as a hexadecimal value (starting with '0x'). (test.S)
## Solución
asm3 trabaja a nivel de bytes sobre los argumentos tomados de la pila (little-endian). El código: pone eax=0, carga en ah el byte [ebp+0xa] (0x75), hace shl ax,0x10 (desplazar un registro de 16 bits 16 posiciones deja ax=0), luego al = 0 - [ebp+0xc] (0x76) = 0x8a, ah = 0 + [ebp+0xd] (0x16) = 0x16, y finalmente xor ax con la palabra [ebp+0x10] (0x1af6). Resultado: 0x168a xor 0x1af6 = 0x0c7c:

0xc7c
## Notas Adicionales
- La clave es el shl ax,0x10 sobre un registro de 16 bits, que lo pone a cero antes de las operaciones por byte.
- Lo confirmé con un modelo en Python respetando los acarreos de 8 y 16 bits.
## Referencias
