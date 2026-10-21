Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye here.
## Solución
Descargué flag.png. Con binwalk vi que después del final del PNG había un archivo ZIP pegado. Lo descomprimí directamente (unzip flag.png avisa de bytes extra al inicio pero extrae igual) y salió una carpeta secret/ con otra imagen flag.png que tenía la flag escrita:

academy{Hiddinng_An_imag3_within_@n_ima9e_c55a7afe}
## Notas Adicionales
- Comandos: binwalk flag.png ; unzip flag.png (o binwalk -e flag.png)
## Referencias
