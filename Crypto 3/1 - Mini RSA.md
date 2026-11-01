Decrypt my super sick RSA. (N, e, c con e pequeño)
## Solución
Descargué los valores con N, e=3 y c. Con un exponente tan chico (e=3) y un mensaje corto, m^3 es menor que N y nunca se reduce módulo N, así que c = m^3 directo. Para recuperar m basta sacar la raíz cúbica entera exacta de c (sin factorizar N):

academy{e_sh0u1d_b3_lArg3r_35f26e1a}
## Notas Adicionales
- Raíz cúbica entera por búsqueda binaria; luego m.to_bytes(...) a texto.
- Mismo problema que "Crack the Power": exponente público demasiado pequeño.
## Referencias
