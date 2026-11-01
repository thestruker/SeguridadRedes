Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints. Read the source code for each vault to figure out the password. VaultDoorTraining.java
## Solución
Descargué VaultDoorTraining.java. El programa toma la contraseña, le quita el prefijo academy{ y la llave de cierre, y compara lo de adentro contra un literal. La contraseña está escrita directamente en el código (hardcoded) en el método checkPassword:

password.equals("w4rm1ng_Up_w1tH_jAv4_4cfa5369b93")

Envolviéndola en el formato de la flag:

academy{w4rm1ng_Up_w1tH_jAv4_4cfa5369b93}
## Notas Adicionales
- Lección: guardar contraseñas en texto plano dentro del código fuente (hardcoded credentials, CWE-798) es inseguro: cualquiera con el código la ve.
## Referencias
