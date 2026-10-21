Now you DON'T see me. This report has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
## Solución
Descargué Financial_Report_for_ABC_Labs.pdf. Visualmente tenía varias partes tapadas con rectángulos negros, pero esa "censura" solo era un dibujo encima del texto, el texto seguía en el PDF. Extraje el texto con pdftotext (también sirve seleccionar todo y copiar) y apareció lo que estaba debajo de las barras negras, incluida la flag:

academy{C4n_Y0u_S33_m3_fully}
## Notas Adicionales
- Comando: pdftotext Financial_Report_for_ABC_Labs.pdf -
- Lección: tapar texto con figuras no es redactar; hay que eliminar el texto realmente.
## Referencias
