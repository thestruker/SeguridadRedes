Can you break into this super secure portal?
## Solución
Inspeccionar la para revisar que hace el boton login
```
 function verify() {

    checkpass = document.getElementById("pass").value;

    split = 4;

    if (checkpass.substring(0, split) == 'pico') {

      if (checkpass.substring(split*6, split*7) == 'eb02') {

        if (checkpass.substring(split, split*2) == 'CTF{') {

         if (checkpass.substring(split*4, split*5) == 'ts_p') {

          if (checkpass.substring(split*3, split*4) == 'lien') {

            if (checkpass.substring(split*5, split*6) == 'lz_2') {

              if (checkpass.substring(split*2, split*3) == 'no_c') {

                if (checkpass.substring(split*7, split*8) == 'b45}') {

                  alert("Password Verified")

                  }

                }

              }

            }

          }

        }

      }

    }

    else {

      alert("Incorrect password");

    }

  }
```
Obtener la contraseña usando el algoritmo que uso:  picoCTF{no_clients_plz_2eb02b45}
## Notas Adicionales
- **Posición `0` a `4` (`0` a `split`):** `pico`
    
- **Posición `4` a `8` (`split` a `split*2`):** `CTF{`
    
- **Posición `8` a `12` (`split*2` a `split*3`):** `no_c`
    
- **Posición `12` a `16` (`split*3` a `split*4`):** `lien`
    
- **Posición `16` a `20` (`split*4` a `split*5`):** `ts_p`
    
- **Posición `20` a `24` (`split*5` a `split*6`):** `lz_2`
    
- **Posición `24` a `28` (`split*6` a `split*7`):** `eb02`
    
- **Posición `28` a `32` (`split*7` a `split*8`):** `b45}`

## Referencias

