Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.

The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.
## Solución
- **Endpoint localizado**: Descarga del archivo `heapdump-1791098797796.heapsnapshot` desde la API de la aplicación.

- **Comando de extracción**:

 ```
 grep -a "academy{" heapdump-1791098797796.heapsnapshot
 ```

- **Flag**: `academy{Pat!3nt_15_Th3_K3y_1dc68c38}`

## Notas Adicionales


## Referencias
