We made a lot of substitutions to encrypt this. Can you decrypt it? (nc a la instancia)
## Solución
Lancé la instancia y me conecté con nc. El servidor manda un texto en inglés cifrado con sustitución monoalfabética (cada letra cambia por otra fija). La primera línea tenía la forma "xxxxxxxx xxxx xx xxxx xxxx - xxxxxxxxx_xx_x_xxxx_xxxxxx_xxxxxxxxxx", que corresponde a "congrats here is your flag - frequency_is_c_over_lambda_...". Con eso saqué buena parte del mapeo, y el resto lo completé con palabras del cuerpo del texto (es el inicio de Drácula: "HAVING HAD SOME TIME AT MY DISPOSAL...", "WHEN", "FOREKNOWLEDGE", etc.). Aplicando el mapeo completo con tr, la flag quedó:

frequency_is_c_over_lambda_lrwpcbmnsy
## Notas Adicionales
- La pista dice "Flag is not in the usual flag format": se envía sin academy{}. Con academy{...} la marcó incorrecta.
- Cada instancia usa un mapeo distinto, pero el texto y la flag descifrada son los mismos.
## Referencias
