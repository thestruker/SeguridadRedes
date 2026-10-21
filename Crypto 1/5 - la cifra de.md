I found this cipher in an old book. Can you figure out what it says? (nc a la instancia)
## Solución
Lancé la instancia y me conecté con nc; el servidor devuelve un texto largo cifrado. El nombre del reto ("La cifra del Sig. Giovan Battista Bellaso") apunta al cifrado de Vigenère. Usé texto plano conocido: la línea "Ne iy nytkwpsznyg nth it mtsztcy..." tenía que ser "It is interesting how in history...". Restando letra a letra (cifrado - plano) obtuve la llave: "flag". Descifré todo el texto con esa llave, aplicándola solo sobre letras ASCII (las letras acentuadas como "è" no avanzan la llave, si no se desfasa). El texto habla de la historia del cifrado de Vigenère y en medio venía la flag:

academy{b311a50_0r_v1gn3r3_c1ph3r623c515c}
## Notas Adicionales
- Llave: flag. Detalle importante: no contar caracteres no ASCII al avanzar el índice de la llave.
## Referencias
