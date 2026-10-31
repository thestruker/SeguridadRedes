You've stumbled upon a peculiar PDF filled with what seems like nothing more than garbled nonsense... uncover the flag within the metadata.
## Solución
Descargué confidential.pdf. El contenido visible era texto sin sentido, así que revisé los metadatos con exiftool. El campo Author tenía una cadena en Base64 (YWNhZGVteXtwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV8yZDk0NzM4NX0=). Al decodificarla salió la flag:

academy{puzzl3d_m3tadata_f0und!_2d947385}
## Notas Adicionales
- Comandos: exiftool confidential.pdf | grep Author ; echo <cadena> | base64 -d
## Referencias
