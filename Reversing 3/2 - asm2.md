What does asm2(0x4,0x1f) return? Submit the flag as a hexadecimal value (starting with '0x'). (test.S)
## Solución
asm2 es un bucle. Inicializa una variable con el segundo argumento (0x1f = 31) y un contador con el primero (0x4 = 4). En cada vuelta suma 1 a la variable y 0xf2 (242) al contador, y repite mientras el contador sea <= 0x3ae2 (15074). El contador toma los valores 4, 246, 488, ... = 4 + 242k; la última vuelta válida es k=62, así que el cuerpo se ejecuta 63 veces. La variable de retorno vale 31 + 63 = 94 = 0x5e:

0x5e
## Notas Adicionales
- Lo verifiqué con una simulación corta en Python del mismo bucle.
- 31 + 63 = 94 = 0x5e.
## Referencias
