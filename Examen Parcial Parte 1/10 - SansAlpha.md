The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.
## Solución
Para resolver el reto **SansAlpha** de picoCTF 2024, donde la shell restringe el uso de cualquier carácter alfabético (`a-z`, `A-Z`), se utilizó la expansión de comodines (_globbing_) de Bash y la especificación de patrones con corchetes y negación usando únicamente números y símbolos.

1. Identifiqué la ubicación del archivo objetivo dentro del directorio local mediante la expansión de rutas `*/*`, confirmando que el archivo se encontraba en `blargh/flag.txt` (una carpeta de 6 caracteres y un archivo de 8 caracteres incluyendo el punto).
    
2. Para leer el contenido del archivo sin usar letras, se buscó invocar el binario `/bin/base64`. Para evitar que la shell seleccionara `/bin/base32` o `/bin/x86_64` por orden alfabético al expandir `/???/??????`, utilicé una clase de caracteres con negación `[!_]`.
    
3. Ejecuté el siguiente comando compuesto únicamente por símbolos y números en la terminal:
    


```
/???/???[!_]64 ??????/????.???
```

- `/???/` resuelve a `/bin/`.
    
- `???[!_]64` fuerza la coincidencia con un ejecutable de 6 caracteres que termine en `64` y cuyo cuarto carácter **no** sea un guion bajo `_` (descartando `/bin/x86_64` y ejecutando directamente `/bin/base64`).
    
- `??????/????.???` apunta a `blargh/flag.txt`.
    

4. Al ejecutar el comando, la shell devolvió la flag codificada en Base64:
    


```
cmV0dXJuIDAgYWNhZGVteXs3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV85Yjc2N2YwN30=
```

5. Decodifiqué la salida resultante en Base64 para obtener la flag final en texto plano:
    

`academy{7h15_mu171v3r53_15_m4dn355_9b767f07}`

## Notas Adicionales


## Referencias
