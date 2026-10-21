I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead? You can download the challenge files here: challenge.zip
## Solución
Descargué challenge.zip y al descomprimirlo salió home/ctf-player/drop-in/flag.png, que era un código QR. Lo decodifiqué (con zbarimg o con el lector de QR de OpenCV) y el contenido del QR era la flag:

academy{p33k_@_b00_a2658a69}
## Notas Adicionales
- Comando: zbarimg flag.png (en la instancia del reto viene instalado). No hizo falta lanzar la instancia, bastó con el zip.
## Referencias
