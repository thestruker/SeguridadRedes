I've hidden a flag in this file. Can you find it? Forensics_is_fun.pptm
## Solución
Descargué Forensics_is_fun.pptm. Los archivos de Office modernos (.pptx/.pptm) en realidad son ZIP, así que lo descomprimí con unzip. Además de las diapositivas y del vbaProject.bin (la macro, que era un distractor), dentro de ppt/slideMasters/ había un archivo extraño llamado "hidden" sin extensión. Contenía una cadena de letras separadas por espacios; al quitar los espacios era Base64. Decodificándola (agregando el padding "=" faltante) salió:

flag: academy{D1d_u_kn0w_ppts_r_z1p5}
## Notas Adicionales
- Comando: tr -d ' ' < ppt/slideMasters/hidden | base64 -d
- Lección: los documentos OOXML son ZIP y pueden esconder archivos que PowerPoint no muestra.
## Referencias
