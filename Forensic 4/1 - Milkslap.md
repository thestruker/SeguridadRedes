🥛 (el reto solo da un enlace a una página web al lanzar la instancia)
## Solución
Lancé la instancia y abrí la página "MilkSlap!", que anima una imagen al mover el mouse. Revisando el código fuente vi que style.css usa como fondo una imagen gigante, concat_v.png (1280x47520, ~18 MB): todos los frames del video pegados verticalmente. La descargué y, como el reto es de esteganografía, revisé los bits menos significativos (LSB) de cada canal. En el canal azul (b1,b,lsb,xy en zsteg), leyendo el LSB pixel por pixel desde la esquina superior izquierda y agrupando de 8 en 8 bits, salió la flag en texto:

academy{imag3_m4n1pul4t10n_sl4p5}
## Notas Adicionales
- zsteg concat_v.png lo detecta como b1,b,lsb,xy. En el webshell zsteg se queda sin memoria por el tamaño de la imagen, así que lo extraje con Python (numpy + Pillow) solo sobre el canal azul.
## Referencias
