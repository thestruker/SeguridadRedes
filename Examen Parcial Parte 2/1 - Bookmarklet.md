Why search for the flag when I can make a bookmarklet to print it for me?
## Solución
Ingresé al sitio web del reto, copié el código JavaScript del marcador (_bookmarklet_) y lo ejecuté directamente dentro de la consola del navegador (**F12** -> **Console**).

El script procesó los caracteres de la cadena cifrada aplicando la clave `"picoctf"` mediante restas modulares de código ASCII/UTF-8 y desplegó la flag directamente en una alerta en pantalla:

`academy{p@g3_turn3r_1b8cd5e0}`

## Notas Adicionales


## Referencias
