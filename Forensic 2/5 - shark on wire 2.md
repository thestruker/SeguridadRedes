We found this packet capture. Recover the flag that was pilfered from the network.
## Solución
Descargué el .pcap y lo analicé. A diferencia del shark on wire 1, aquí había muchísimos streams señuelo (incluso dos que deletreaban flags falsas: academy{StaT31355_636f6e6e} —la de shark 1— y academy{N0t_a_fLag}). La clave estaba en dos paquetes marcadores: uno con el payload "start" y otro con "end", ambos hacia 10.0.0.1 puerto 22. Entre esos dos marcadores, todos los paquetes iban a 10.0.0.1:22 y el carácter de la flag estaba escondido en el PUERTO DE ORIGEN de cada paquete: cada carácter = (puerto_origen - 5000). Decodificando los puertos origen en orden de captura salió la flag:

academy{p1LLf3r3d_data_v1a_st3g0}
## Notas Adicionales
- Canal encubierto: el dato no estaba en el payload sino en el source port (char = sport - 5000).
- Los marcadores "start"/"end" delimitan la ventana de exfiltración hacia 10.0.0.1:22.
## Referencias
