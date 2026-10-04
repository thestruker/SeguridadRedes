Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!

Download the Rust code [here](https://challenge-files.cylabacademy.net/library/b9cfc84c442958b8ac848ddc0692bed9ef01a15877b8d37f36afbe68b5849acc/fixme1.tar.gz).
## Solución
Primero corregí los errores de sintaxis en el archivo `main.rs`: agregué los puntos y coma `;` faltantes, cambié `ret` por `return` e invoqué correctamente la macro `println!` usando `{}` para dar formato a la cadena descifrada.

Luego compilé y ejecuté el programa usando Cargo:

```
dastruker-academy@webshell:~$ cargo run
   Compiling challenge v0.1.0 (/home/dastruker-academy/challenge)
    Finished dev [unoptimized + debuginfo] target(s) in 0.45s
     Running `target/debug/challenge`
academy{4r3_y0u_4_ru$t4c30n_n0w?}
```

Al ejecutar el código corregido, el programa procesó los bytes en hexadecimal con la clave `CSUCKS`, descifró el vector de bytes usando `XORCryptor` y mostró la flag directamente en la pantalla: `academy{4r3_y0u_4_ru$t4c30n_n0w?}`

## Notas Adicionales


## Referencias
