We found this packet capture. Recover the flag.
## Solución
Descargué el archivo .pcap y lo analicé revisando el tráfico de red. Filtrando por UDP vi varias conversaciones; en el puerto 8888 había dos flujos de datos, uno era un señuelo (academy{N0t_a_fLag}). En el flujo dirigido a la IP 10.0.0.12 cada paquete llevaba un solo carácter en su payload, así que junté esos caracteres en orden y formaron la flag:

academy{StaT31355_636f6e6e}
## Notas Adicionales
- La pista está en seguir el stream UDP del puerto 8888 hacia 10.0.0.12 (el de 10.0.0.13 era falso).
## Referencias
