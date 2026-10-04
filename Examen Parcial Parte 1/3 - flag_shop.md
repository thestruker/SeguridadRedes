There's a flag shop selling stuff, can you buy a flag?
## Solución
Primero me conecté al servicio de la tienda mediante netcat:

```
┌──(dastruker㉿MSI)-[/mnt/c/Users/adomi]
└─$ nc chatelaine.cylabacademy.net 10528
```

Entré a la sección de compras (`2. Buy Flags`) y elegí la bandera falsa (`1. Defintely not the flag Flag`). Para aprovechar la vulnerabilidad de desbordamiento de enteros (_Integer Overflow_), ingresé una cantidad muy grande de banderas (`22222685678`):

```
These knockoff Flags cost 900 each, enter desired quantity
22222685678

The final cost is: -1245587272

Your current balance after transaction: 1245588372
```

Al multiplicar esa cantidad por el precio de 900, el número superó el límite del entero de 32 bits y se volvió negativo (`-1245587272`). Como la tienda resta el costo total de tu saldo, terminar sumando esa cantidad y mi balance aumentó a más de 1.2 mil millones de monedas.

Con el saldo inflado, volví a la tienda, seleccioné la bandera real (`2. 1337 Flag`) e ingresé `1` para comprarla, obteniendo la flag:

```
YOUR FLAG IS: academy{m0n3y_bag5_CAec77CC}
```

## Notas Adicionales


## Referencias
