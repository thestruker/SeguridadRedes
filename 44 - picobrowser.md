This website can be rendered only by picobrowser, go and catch the flag!
## Solución
MSI:/mnt/host/c/Users/adomi# curl -s http://fickle-tempest.picoctf.net:57911/flag -H "User-Agent: picobrowser" | grep pi
co
         <!-- <strong>Title</strong> --> picobrowser!
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}</code></p>

## Notas Adicionales
Usamos curl con -s para conectar con el url y ejecutar cambios que hagamos dentro de los response de la pagina pero de manera silenciosa con el -s

## Referencias


