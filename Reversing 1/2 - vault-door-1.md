This vault uses some complicated arrays! VaultDoor1.java
## Solución
Descargué VaultDoor1.java. El método checkPassword exige que la contraseña tenga 32 caracteres y comprueba cada posición con password.charAt(i) == 'x', pero en desorden para despistar. Saqué cada par (índice, carácter) con una expresión regular y los ordené por índice para reconstruir la cadena:

academy{d35cr4mbl3_tH3_cH4r4cT3r5_45ebc3}
## Notas Adicionales
- charAt(i) devuelve el carácter en la posición i. El orden de las condiciones con && no cambia el resultado, así que ordenando por índice sale la contraseña.
## Referencias
