Oops! I have a typo in my first message so i sent it again! I used RSA twice so this is secure right?
## Solución
chall.py cifra dos mensajes con el mismo N y e=17, y output.txt da c1, c2, la diferencia M - M_fixed = -3 y N. Como los mensajes están relacionados linealmente (M_fixed = M + 3), se aplica el ataque de Franklin-Reiter: el mensaje es raíz común de f1(x)=x^17-c1 y f2(x)=(x+3)^17-c2 mod N, así que el MCD de los polinomios es (x - M). Implementé el MCD de polinomios mod N y obtuve M = "academy{m3ssage_w1th_typ0z" (el que tenía la errata); el corregido es M+3, que cambia la "z" por "}":

academy{m3ssage_w1th_typ0}
## Notas Adicionales
- Ataque Franklin-Reiter de mensajes relacionados.
## Referencias
