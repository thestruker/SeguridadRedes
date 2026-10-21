Theres tapping coming in from the wires. What's it saying? (nc a la instancia)
## Solución
Lancé la instancia y me conecté con nc; el servidor imprimió una cadena de puntos y rayas separados por espacios, con llaves en medio: código Morse. Lo decodifiqué con un pequeño script de Python (diccionario Morse → letra/número). Morse no distingue mayúsculas/minúsculas, así que la flag sale en mayúsculas:

ACADEMY{M0RS3C0D31SFUNA3B0BAF8}
## Notas Adicionales
- Se envía tal cual en mayúsculas.
## Referencias
