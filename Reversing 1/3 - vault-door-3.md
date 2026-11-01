This vault uses for-loops and byte arrays. VaultDoor3.java
## Solución
Descargué VaultDoor3.java. Aquí la contraseña (32 chars) se reordena en un buffer con varios for: los primeros 8 se copian igual, los siguientes 8 en orden inverso (23-i), luego las posiciones pares con 46-i y al final las impares de 17 a 31 tal cual. El buffer resultante debe ser igual a "jU5t_a_sna_3lpm16gd4e_u_4_m7re42". Invertí la permutación (por cada índice del buffer, coloqué el carácter en la posición original de la contraseña) y obtuve:

academy{jU5t_a_s1mpl3_an4gr4m_4_u_e7de62}
## Notas Adicionales
- Es un anagrama: el texto del buffer está revuelto; deshaciendo el mapeo de los for se recupera la contraseña real.
## Referencias
