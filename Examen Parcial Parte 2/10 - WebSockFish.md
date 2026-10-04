Can you win in a convincing manner against this chess bot? He won't go easy on you!
## Solución
Ingresé al sitio del reto y revisé el código fuente para entender cómo se comunicaba el cliente con el servidor mediante WebSocket. Encontré que el cliente enviaba al servidor la evaluación de la partida con mensajes como `eval <valor>`. Aprovechando esto, envié directamente `eval -100000` mediante la consola del navegador, haciendo que el servidor considerara que el bot estaba perdiendo y se rindiera automáticamente. Finalmente, obtuve la flag `academy{c1i3nt_s1d3_w3b_s0ck3t5_96466159}`.

## Notas Adicionales


## Referencias
chat gpt