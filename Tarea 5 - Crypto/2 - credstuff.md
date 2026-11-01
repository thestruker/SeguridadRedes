leak.tar
## Solución
Descargué y extraje leak.tar, que trae usernames.txt y passwords.txt (la línea N de uno corresponde a la línea N del otro). Busqué al usuario cultiris con grep -n y estaba en la línea 378; esa misma línea en passwords.txt tenía npnqrzl{P7e1S_54I35_71Z3}. Al notar que npnqrzl en ROT13 es "academy", apliqué ROT13 a toda la contraseña:

academy{C7r1F_54V35_71M3}
## Notas Adicionales
- grep -n "cultiris" leak/usernames.txt da el número de línea; sed -n '378p' leak/passwords.txt la contraseña.
## Referencias
