We found this packet capture and key. Recover the flag.
## Solución
Descargué webnet0-capture.pcap y picopico.key. Al abrir la captura todo el tráfico era TLS hacia el puerto 443, así que no se veía nada en claro. Revisé el Server Hello y el cipher suite era 0x009d (TLS_RSA_WITH_AES_256_GCM_SHA384), que usa intercambio de llaves RSA (sin forward secrecy), por lo que con la llave privada del servidor se puede descifrar toda la sesión. Cargué picopico.key en Wireshark (Preferences → Protocols → TLS → RSA keys list: puerto 443, protocolo http) y apareció el tráfico HTTP descifrado. En los encabezados de la respuesta del servidor venía un header personalizado "Pico-Flag" con la flag:

academy{nongshim.shrimp.crackers}
## Notas Adicionales
- Equivalente en terminal: tshark -r webnet0-capture.pcap -o "tls.keys_list:any,443,http,picopico.key" -Y http -V | grep Pico-Flag
- Funciona porque el cipher usa RSA key exchange; con ECDHE no bastaría la llave privada.
## Referencias
