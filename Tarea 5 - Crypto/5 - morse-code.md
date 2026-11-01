morse_chal.wav
## Solución
Descargué morse_chal.wav, un audio mono de ~29 s. Contiene código Morse en la señal: analicé la energía del audio en ventanas de ~10 ms con Python (wave + numpy) para separar tonos cortos (punto), largos (raya) y silencios (separadores). Traduciendo los puntos y rayas a letras salió el mensaje; Morse va en mayúsculas:

academy{WH47_H47H_90D_W20U9H7}
## Notas Adicionales
- La duración de cada tono distingue punto/raya; los silencios separan letras y palabras.
## Referencias
