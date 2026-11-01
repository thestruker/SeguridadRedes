This vault converts numbers into different bases. VaultDoor4.java
## Solución
Descargué VaultDoor4.java. La contraseña se compara byte a byte contra un arreglo myBytes donde cada byte está escrito en una base distinta para confundir: decimal (106, 85...), hexadecimal (0x55, 0x6e...), octal (0142, 0131...) y caracteres ('8', '4'...). Convertí cada valor a su carácter ASCII:

academy{jU5t_4_bUnCh_0f_bYt3s_2a84ec9f20}
## Notas Adicionales
- 106=j, 85=U, 0x55=U, 0142(octal)=b, '8'=8, etc. Todo es el mismo valor escrito en bases diferentes.
## Referencias
