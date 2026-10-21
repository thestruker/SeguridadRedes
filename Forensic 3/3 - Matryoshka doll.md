Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: dolls.jpg
## Solución
Descargué dolls.jpg. Aunque se abría como imagen normal, con binwalk vi que al final traía un archivo ZIP pegado (la firma PK). Como un ZIP se lee desde el final del archivo, se puede descomprimir directamente con unzip dolls.jpg. Adentro venía base_images/2_c.jpg, que a su vez tenía otro ZIP escondido; repetí el proceso: 2_c.jpg → 3_c.jpg → 4_c.jpg, y al descomprimir la última muñeca salió flag.txt con la flag:

academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}
## Notas Adicionales
- binwalk -e dolls.jpg también extrae cada nivel; fueron 4 niveles de imágenes anidadas.
- Técnica: archivos políglota (JPG + ZIP concatenados).
## Referencias
