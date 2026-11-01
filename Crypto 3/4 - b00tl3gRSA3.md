Connect to the service to get c, n and e=65537.
## Solución
Me conecté con nc a la instancia (c, n, e=65537). El módulo n no es producto de dos primos grandes sino de muchos primos pequeños (~34 bits cada uno), así que se factoriza completo en segundos con Pollard rho. Con todos los factores calculé la función de Carmichael lambda(n) = mcm(p_i - 1), luego d = inverso de e módulo lambda(n) y descifré m = c^d mod n:

academy{too_many_fact0rs_5984067}
## Notas Adicionales
- Muchos primos pequeños = factorización trivial con Pollard rho.
- Con n squarefree se usa lambda(n)=lcm(p_i-1) en lugar de phi; d=pow(e,-1,lambda).
## Referencias
