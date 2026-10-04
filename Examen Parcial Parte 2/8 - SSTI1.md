I made a cool website where you can announce whatever you want! Try it out!
## Solución
Ingresé al sitio del reto y probé el campo de anuncio con `{{7*7}}`, obteniendo `49`, por lo que confirmé que la página interpretaba expresiones de plantilla. Después aproveché la vulnerabilidad SSTI de Jinja2 para ejecutar comandos en el servidor, utilizando `cat flag` para consultar el archivo que contenía la flag. Finalmente, obtuve `academy{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_dee0a1a6}`.

## Notas Adicionales


## Referencias
