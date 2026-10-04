The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?
## Solución
Primero corregí los errores de préstamos (_borrowing_) y mutabilidad en el archivo `src/main.rs`: declaré la variable `party_foul` como mutable (`let mut party_foul`), cambié su paso a la función por una referencia mutable (`&mut party_foul`) y actualicé la firma del parámetro en `decrypt` a `borrowed_string: &mut String` para permitir el uso del método `.push_str()`.

Luego compilé y ejecuté el programa usando Cargo:

```
dastruker-academy@webshell:~$ cargo run
   Compiling rust_proj v0.1.0 (/home/dastruker-academy/fixme2)
    Finished dev [unoptimized + debuginfo] target(s) in 0.45s
     Running `target/debug/rust_proj`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}
```

Al ejecutar el programa corregido con los préstamos mutables válidos de Rust, la función `decrypt` modificó la cadena, descifró los bytes en hexadecimal y mostró la flag directamente en la pantalla: `picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}`


## Notas Adicionales


## Referencias
