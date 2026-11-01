Base 64 is like eight times stronger, right? VaultDoor5.java
## Solución
Descargué VaultDoor5.java. La contraseña pasa por dos codificaciones: primero URL-encode de cada byte (%xx) y luego Base64 de ese resultado, y se compara contra una cadena "expected". Para recuperar la contraseña hice el proceso inverso: decodifiqué el Base64 y luego el URL-encoding:

academy{c0nv3rt1ng_fr0m_ba5e_64_e340c3ed}
## Notas Adicionales
- Comando equivalente: echo '<expected>' | base64 -d, y después decodificar los %xx (URL decode).
- Codificar no es cifrar: Base64 y URL-encode son reversibles sin ninguna llave.
## Referencias
