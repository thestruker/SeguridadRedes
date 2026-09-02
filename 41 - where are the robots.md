Can you find the robots?
## Solución
Preguntar a la IA Gemini sobre los robots
solo agregar la extencion de robots al final del link
```
http://fickle-tempest.picoctf.net:63457/robots.txt

y mostrara la ruta oculta

http://fickle-tempest.picoctf.net:63457/cc6b1.html

Guess you found the robots  
picoCTF{ca1cu1at1ng_Mach1n3s_cc6b1}
```
## Notas Adicionales
La pista pregunta: _¿Qué parte del sitio web podría decirte dónde el creador no quiere que mires?_

En desarrollo web existe un archivo público llamado **`robots.txt`**. Su propósito es indicar a los rastreadores (como Googlebot) qué páginas o secciones del sitio **no** deben ser indexadas (usando la directiva `Disallow`). Los atacantes y pentesters siempre revisan este archivo porque a menudo revela rutas o archivos "ocultos" o sensibles.

si escribo curl en terminal y despues el link, me da el html de la pagina y si despues le agrego | grep pico podria obtener la flag

## Referencias
