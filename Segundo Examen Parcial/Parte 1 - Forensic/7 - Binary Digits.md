This file doesn't look like much... just a bunch of 1s and 0s.
## Solución
Descargué digits.bin, que era texto con solo caracteres 0 y 1 (71424 dígitos). Agrupando de 8 en 8 y convirtiendo cada grupo a un byte, los primeros bytes fueron FF D8 FF E0 ... JFIF: un JPEG. Lo guardé como imagen y al abrirlo se veía la flag:

academy{h1dd3n_1n_th3_b1n4ry_fd12019b}
## Notas Adicionales
- Python: bytes(int(b[i:i+8],2) for i in range(0,len(b),8))
## Referencias
