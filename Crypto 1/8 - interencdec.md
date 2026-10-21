Can you get the real meaning from this file.
## Solución
Descargué enc_flag, que contenía YidhR3BvYTJ4MFpudHFhR3g2YUhsZmF6TnFlVGwzWVROclh6azVORGhyYldneWZRPT0nCg==. Al decodificar de Base64 salió b'aGpoa2x0ZntqaGx6aHlfazNqeTl3YTNrXzk5NDhrbWgyfQ==' (la representación de un bytes de Python, con otro Base64 dentro). Decodifiqué otra vez ese Base64 interno y obtuve hjhkltf{jhlzhy_k3jy9wa3k_9948kmh2}, que parece flag pero con las letras corridas: es un César. Probando los desplazamientos, con 7 hacia atrás quedó:

academy{caesar_d3cr9pt3d_9948dfa2}
## Notas Adicionales
- Capas: Base64 → Base64 → César (shift 7).
## Referencias
