This service can provide you with a random number, but can it do anything else? (picker-I.py)
## Solución
El servicio lee una línea y ejecuta eval(user_input + '()'), es decir, llama como función lo que uno escriba. En el código fuente hay una función win() que imprime la bandera. Como no hay ningún filtro, basta con conectarse por nc y enviar win para que la ejecute. La flag sale impresa en hexadecimal (bytes 0x..), que luego convertí a texto:

academy{4_d14m0nd_1n_7h3_r0ugh_c55fbef5}
## Notas Adicionales
- Vulnerabilidad: eval() sobre entrada del usuario permite invocar cualquier función del programa.
- Enviar win por nc y decodificar los bytes hex devueltos.
## Referencias
