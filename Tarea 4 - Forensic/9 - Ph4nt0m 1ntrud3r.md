A digital ghost has breached my defenses, and my sensitive data has been stolen! Analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner.
## Solución
Descargué myNetworkTraffic.pcap y lo abrí en Wireshark. Eran paquetes TCP sueltos cuyo payload era una cadena corta en Base64. La pista "well timely manner" indicaba que había que ordenarlos por tiempo (el orden en el archivo estaba revuelto). Ordenando por frame.time, los primeros paquetes eran basura (Base64 de bytes aleatorios terminados en un solo "="), y los últimos, terminados en "==", decodificaban a fragmentos de texto: "academy", "{1t_w4s", "nt_th4t", "_34sy_t", "bh_4r_a", "8139a41", "}". Concatenándolos:

academy{1t_w4snt_th4t_34sy_tbh_4r_a8139a41}
## Notas Adicionales
- Comando: tshark -r myNetworkTraffic.pcap -T fields -e frame.time_epoch -e tcp.payload | sort -n, luego hex → texto → base64 -d.
## Referencias
