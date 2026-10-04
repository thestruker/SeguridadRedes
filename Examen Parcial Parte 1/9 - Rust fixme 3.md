Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!

Download the Rust code [here](https://challenge-files.cylabacademy.net/library/6df8b7779faf29e53f515922041d99bc26381a332ca090c291ba20577ac7cf92/fixme3.tar.gz).
## Solución
Solución Primero corregí la sintaxis del archivo `src/main.rs` descomentando el cierre de la llave del bloque `unsafe { ... }`. Esto permitió envolver adecuadamente la llamada a la función no segura `std::slice::from_raw_parts`, la cual exige un entorno `unsafe` en Rust al manipular punteros _raw_.

Luego compilé y ejecuté el programa usando Cargo:

Al ejecutar el programa corregido, el código dentro del bloque `unsafe` reconstruyó el _slice_ de bytes desde el puntero, descifró el vector con la clave `CSUCKS` y mostró la flag directamente en la pantalla: `academy{n0w_y0uv3_f1x3d_1h3m_411}`
## Notas Adicionales


## Referencias
