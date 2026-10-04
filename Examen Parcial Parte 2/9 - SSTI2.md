I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)
## Solución
Ingresé al sitio del reto y comprobé que existía una vulnerabilidad SSTI utilizando `{{2*2}}` y `{{request}}`. Después identifiqué que la aplicación tenía un filtro para bloquear ciertos caracteres y palabras, por lo que utilicé `attr()` y representaciones alternativas de los caracteres para evadirlo. Con este bypass pude acceder a funciones de Python y ejecutar `cat flag` en el servidor. Finalmente, obtuve la flag `academy{sst1_f1lt3r_byp4ss_26c3eb41}`.

## Notas Adicionales


## Referencias
