message.txt (sin clave)
## Solución
Descargué message.txt, un texto cifrado por sustitución monoalfabética pero esta vez sin dar la clave. Usé análisis de frecuencias: las letras más comunes del inglés (e, t, a, o...) corresponden a las más frecuentes del cifrado, y ajustando el mapeo con palabras reconocibles reconstruí la sustitución completa hasta leer la flag:

academy{FR3QU3NCY_4774CK5_4R3_C001_7B0043A0}
## Notas Adicionales
- Frequency attack: la distribución de letras del cifrado delata el mapeo cuando el texto es largo.
## Referencias
